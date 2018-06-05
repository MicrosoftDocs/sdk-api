---
UID: NF:mi.MI_OperationOptions_GetOptionAt
title: MI_OperationOptions_GetOptionAt function
author: windows-sdk-content
description: Gets a previously added option value based on the specified index.
old-location: wmi_v2\mi_operationoptions_getoptionat.htm
old-project: wmi_v2
ms.assetid: 06ae674b-c7d7-47c1-81f2-6a825d9889a2
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_OperationOptions_GetOptionAt, MI_OperationOptions_GetOptionAt function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetOptionAt, wmi_v2.mi_operationoptions_getoptionat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_OperationOptions_GetOptionAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_GetOptionAt function


## -description


Gets a previously added option value based on the specified index.


## -parameters




### -param options [in]

MI_OperationOptions structure.


### -param index

Zero-based index of the option.


### -param optionName

Returned option name.


### -param value [out]

Returned option value.


### -param type [out]

Returned option type.


### -param flags [out, optional]

Returned option flags.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



