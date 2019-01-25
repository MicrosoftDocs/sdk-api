---
UID: NF:tapi3if.ITCallInfo.SetCallInfoBuffer
title: ITCallInfo::SetCallInfoBuffer
author: windows-sdk-content
description: The SetCallInfoBuffer method sets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the ITCallInfo::put_CallInfoBuffer method.
old-location: tapi3\itcallinfo_setcallinfobuffer.htm
tech.root: Tapi
ms.assetid: fafe3c99-4584-43eb-b446-a9f2b9308097
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],SetCallInfoBuffer method, ITCallInfo.SetCallInfoBuffer, ITCallInfo::SetCallInfoBuffer, SetCallInfoBuffer, SetCallInfoBuffer method [TAPI 2.2], SetCallInfoBuffer method [TAPI 2.2],ITCallInfo interface, _tapi3_itcallinfo_setcallinfobuffer, tapi3.itcallinfo_setcallinfobuffer, tapi3if/ITCallInfo::SetCallInfoBuffer
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
 - ITCallInfo.SetCallInfoBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo::SetCallInfoBuffer


## -description


The 
<b>SetCallInfoBuffer</b> method sets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">ITCallInfo::put_CallInfoBuffer</a> method.


## -parameters




### -param CallInfoBuffer [in]


<a href="https://msdn.microsoft.com/76774741-2aa3-455c-a203-1daee42cf0fa">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.


### -param dwSize [in]

Size of <i>pCallInfoBuffer</i>.


### -param pCallInfoBuffer [in]

Pointer to call information buffer.


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
The <i>pCallInfoBuffer</i> parameter is not a valid pointer.

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



<a href="https://msdn.microsoft.com/cda9d577-7230-42d9-8063-5ca94e0400dc">get_CallInfoBuffer</a>



<a href="https://msdn.microsoft.com/4404ec08-2443-4d1a-8f94-5eb1b3315169">put_CallInfoBuffer</a>
 

 

