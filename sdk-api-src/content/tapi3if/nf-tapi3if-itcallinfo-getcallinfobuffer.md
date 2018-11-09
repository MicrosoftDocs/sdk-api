---
UID: NF:tapi3if.ITCallInfo.GetCallInfoBuffer
title: ITCallInfo::GetCallInfoBuffer
author: windows-sdk-content
description: The GetCallInfoBuffer method gets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the ITCallInfo::get_CallInfoBuffer method.
old-location: tapi3\itcallinfo_getcallinfobuffer.htm
tech.root: tapi
ms.assetid: 00f5dde6-e9df-4b61-8122-2183e047f9ba
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetCallInfoBuffer, GetCallInfoBuffer method [TAPI 2.2], GetCallInfoBuffer method [TAPI 2.2],ITCallInfo interface, ITCallInfo interface [TAPI 2.2],GetCallInfoBuffer method, ITCallInfo.GetCallInfoBuffer, ITCallInfo::GetCallInfoBuffer, _tapi3_itcallinfo_getcallinfobuffer, tapi3.itcallinfo_getcallinfobuffer, tapi3if/ITCallInfo::GetCallInfoBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo.GetCallInfoBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo::GetCallInfoBuffer


## -description


The 
<b>GetCallInfoBuffer</b> method gets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">ITCallInfo::get_CallInfoBuffer</a> method.


## -parameters




### -param CallInfoBuffer [in]


<a href="https://msdn.microsoft.com/76774741-2aa3-455c-a203-1daee42cf0fa">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.


### -param pdwSize [out]

Size of buffer returned in bytes.


### -param ppCallInfoBuffer [out]

Pointer to buffer containing the needed call information.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The <i>pdwSize</i> or <i>ppCallInfoBuffer</i> parameter is not a valid pointer.

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



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/fafe3c99-4584-43eb-b446-a9f2b9308097">SetCallInfoBuffer</a>



<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">get_CallInfoBuffer</a>



<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">put_CallInfoBuffer</a>
 

 

