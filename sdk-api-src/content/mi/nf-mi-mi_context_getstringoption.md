---
UID: NF:mi.MI_Context_GetStringOption
title: MI_Context_GetStringOption function
author: windows-sdk-content
description: Gets the string option that the client sets, based on the operation name.
old-location: wmi_v2\mi_context_getstringoption.htm
old-project: wmi_v2
ms.assetid: ef6fa103-7421-4c66-902d-c5a731abaa54
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_Context_GetStringOption, MI_Context_GetStringOption function [Windows Management Infrastructure (MI)], mi/MI_Context_GetStringOption, wmi.mi_getstringoption, wmi_v2.mi_context_getstringoption
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Context_GetStringOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_GetStringOption function


## -description


Gets the string option that the client sets, based on the operation name.


## -parameters




### -param context [in]

A pointer to the request context.


### -param name [in]

The name of the option to get.


### -param value

A pointer to the returned option value.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The returned string does not need to be deleted. The string is valid until the provider returns the final result for this operation.



