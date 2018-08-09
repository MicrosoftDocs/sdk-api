---
UID: NF:tapi3if.ITCallInfo.get_CallInfoBuffer
title: ITCallInfo::get_CallInfoBuffer
author: windows-sdk-content
description: The get_CallInfoBuffer method gets call information items which require a buffer, such as user-user information.
old-location: tapi3\itcallinfo_get_callinfobuffer.htm
old-project: tapi
ms.assetid: cda9d577-7230-42d9-8063-5ca94e0400dc
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallInfoBuffer method, ITCallInfo.get_CallInfoBuffer, ITCallInfo::get_CallInfoBuffer, _tapi3_itcallinfo_get_callinfobuffer, get_CallInfoBuffer, get_CallInfoBuffer method [TAPI 2.2], get_CallInfoBuffer method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callinfobuffer, tapi3if/ITCallInfo::get_CallInfoBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo.get_CallInfoBuffer
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallInfo::get_CallInfoBuffer


## -description


The 
<b>get_CallInfoBuffer</b> method gets call information items which require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">ITCallInfo::GetCallInfoBuffer</a> method.


## -parameters




### -param CallInfoBuffer [in]


<a href="https://msdn.microsoft.com/76774741-2aa3-455c-a203-1daee42cf0fa">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.


### -param ppCallInfoBuffer [out]

Pointer to <b>VARIANT</b> representation of call information buffer. The application must call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free the memory allocated for this parameter.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCallInfoBuffer</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoBuffer</i> parameter is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> is not valid for this operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76774741-2aa3-455c-a203-1daee42cf0fa">CALLINFO_BUFFER</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/00f5dde6-e9df-4b61-8122-2183e047f9ba">GetCallInfoBuffer</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">SetCallInfoBuffer</a>



<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">put_CallInfoBuffer</a>
 

 

