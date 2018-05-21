---
UID: NF:mi.MI_OperationOptions_SetCustomOption
title: MI_OperationOptions_SetCustomOption function
author: windows-driver-content
description: Sets a custom option for the operation.
old-location: wmi_v2\mi_operationoptions_setcustomoption.htm
old-project: wmi_v2
ms.assetid: 5db96e9e-dd81-4b62-a555-770b781d0ed3
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_OperationOptions_SetCustomOption, MI_OperationOptions_SetCustomOption function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetCustomOption, wmi_v2.mi_operationoptions_setcustomoption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_OperationOptions_SetCustomOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetCustomOption function


## -description


Sets a  custom option for the operation.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to set.


### -param optionValueType [in]

Option type.


### -param optionValue [in]

New option value.


### -param mustComply

Boolean value where <b>MI_TRUE</b> means that the option must be complied with.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



