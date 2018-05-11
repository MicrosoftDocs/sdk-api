---
UID: NF:mi.MI_OperationOptions_SetString
title: MI_OperationOptions_SetString function
author: windows-driver-content
description: Sets a custom string option.
old-location: wmi_v2\mi_operationoptions_setstring.htm
old-project: wmi_v2
ms.assetid: 1bfc3af0-cc43-4a80-acbe-010520acf8b5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_OperationOptions_SetString, MI_OperationOptions_SetString function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetString, wmi_v2.mi_operationoptions_setstring
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
-	MI_OperationOptions_SetString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetString function


## -description


Sets a custom string option.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option.


### -param value

A null-terminated string that represents the new value for the option.


### -param flags

Option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/1d1b9650-10c3-4e06-a841-6706ecc5f32c">MI_OperationOptions_GetString</a>
 

 

