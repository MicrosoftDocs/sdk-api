---
UID: NF:mi.MI_Context_SetStringOption
title: MI_Context_SetStringOption function
author: windows-sdk-content
description: Sets a context-specific option.
old-location: wmi_v2\mi_context_setstringoption.htm
old-project: wmi_v2
ms.assetid: a7affdbe-1fc7-4662-8f21-077138365adf
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Context_SetStringOption, MI_Context_SetStringOption function [Windows Management Infrastructure (MI)], mi/MI_Context_SetStringOption, wmi.mi_setstringoption, wmi_v2.mi_context_setstringoption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Context_SetStringOption
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_SetStringOption function


## -description


Sets a context-specific option.


## -parameters




### -param context [in]

Request context.


### -param name

A null-terminated string that represents the name of the option to change.


### -param value

A null-terminated string that represents the new value for the specified option.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This function allows the provider to adjust the server's behavior.

On Windows Server 2012, this function only supports the "SECURITY" option, which is used only by an indication provider to control which users have permission to subscribe to the indication class. The function is valid if and only if it is called inside the indication class's *_Load function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/3338ca5c-48ac-450f-bf2a-ded6a2c3da19">MI_Context_GetCustomOption</a>



<a href="https://msdn.microsoft.com/f4f6c935-5207-46f6-b015-c4db724113f3">MI_Context_GetCustomOptionAt</a>



<a href="https://msdn.microsoft.com/8cce1492-5c3a-4ba8-8f33-22f6ff7fcf3a">MI_Context_GetCustomOptionCount</a>



<a href="https://msdn.microsoft.com/862a44b9-a6bd-4433-a7da-9309392a946c">MI_Context_GetNumberOption</a>



<a href="https://msdn.microsoft.com/ef6fa103-7421-4c66-902d-c5a731abaa54">MI_Context_GetStringOption</a>
 

 

