---
title: "ValidateCount Attribute Declaration | Microsoft Docs"
ms.custom: ""
ms.date: "09/13/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords:
  - "attributes, ValidateCount"
  - "ValidateCount attribute, described"
  - "ValidateCount attribute"
ms.assetid: 516af1ef-2c2e-408d-84bc-865f5bccf761
caps.latest.revision: 11
---
# ValidateCount Attribute Declaration

The ValidateCount attribute specifies the minimum and maximum number of arguments allowed for a cmdlet parameter.

## Syntax

```csharp
[ValidateCount(int minLength, int maxlength)]
```

#### Parameters

`MinLength` ([System.Int32](/dotnet/api/System.Int32))
Required. Specifies the minimum number of arguments.

`MaxLength`([System.Int32](/dotnet/api/System.Int32))
Required. Specifies the maximum number of arguments.

## Remarks

- For more information about how to declare this attribute, see [How to Declare Input Validation Rules](http://msdn.microsoft.com/en-us/544c2100-62ba-4be4-b2a2-cc0d4e4fc45b).

- When this attribute is not invoked, the corresponding cmdlet parameter can have any number of arguments.

- The Windows PowerShell runtime throws an error under the following conditions:

    - The `MinLength` and `MaxLength` attribute parameters are not of type [System.Int32](/dotnet/api/System.Int32).

    - The value of the `MaxLength` attribute parameter is less than the value of the `MinLength` attribute parameter.

- The ValidateCount attribute is defined by the [System.Management.Automation.Validatecount](/dotnet/api/System.Management.Automation.ValidateCount) class.

## See Also

[System.Management.Automation.Validatecount](/dotnet/api/System.Management.Automation.ValidateCount)

[How to Declare Input Validation Rules](http://msdn.microsoft.com/en-us/544c2100-62ba-4be4-b2a2-cc0d4e4fc45b)

[Writing a Windows PowerShell Cmdlet](./writing-a-windows-powershell-cmdlet.md)
