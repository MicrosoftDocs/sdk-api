---
UID: NF:mi.MI_Context_WriteError
title: MI_Context_WriteError function
author: windows-sdk-content
description: Sends an error code and error message to the client.
old-location: wmi_v2\mi_context_writeerror.htm
old-project: wmi_v2
ms.assetid: 7626b488-58a3-4c9c-a80b-9b0a6dd7f533
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Context_WriteError, MI_Context_WriteError function [Windows Management Infrastructure (MI)], MI_RESULT_TYPE_HRESULT, MI_RESULT_TYPE_MI, MI_RESULT_TYPE_WIN32, mi/MI_Context_WriteError, wmi.mi_writeerror, wmi_v2.mi_context_writeerror
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
 - MI_Context_WriteError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_WriteError function


## -description


Sends an error code and error message to the client.


## -parameters




### -param context [in]

Request context.


### -param resultCode

Result code to send to the client.


### -param resultType

A null-terminated string that represents the type of the result code, which may (but is not required to) contain one of these values:



#### MI_RESULT_TYPE_MI ("MI")

MI result type.



#### MI_RESULT_TYPE_HRESULT ("HRESULT")

<b>HRESULT</b> (COM return type) result type.



#### MI_RESULT_TYPE_WIN32 ("WIN32")

Win32 result type. See <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.


### -param errorMessage

A null-terminated string that represents the error message to accompany the result code. This message should be localized based on the client's locale request (retrieved through the <a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a> function).


### -param flag [out]

On return, flag contains <b>MI_TRUE</b> if provider should continue execution. Otherwise, the returned value will be <b>MI_FALSE</b>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



The operation is not terminated by this call, although the client has the option to indicate that the operation should be continued or canceled.

If the client does not ask for <b>MI_Context_WriteError</b> messages, the function will give an automatic response.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/7d2271e8-de76-4629-aedc-0ab882ab58eb">MI_Context_GetLocale</a>



<a href="https://msdn.microsoft.com/b52e3b28-a4b7-4017-9670-09b10363544b">MI_Context_PostError</a>
 

 

