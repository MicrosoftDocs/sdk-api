---
UID: NF:ctffunc.ITfCandidateString.GetString
title: ITfCandidateString::GetString (ctffunc.h)
author: windows-sdk-content
description: ITfCandidateString::GetString method
old-location: tsf\itfcandidatestring_getstring.htm
tech.root: TSF
ms.assetid: 157dc848-858c-462f-8e41-78d6bfe20705
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Text Services Framework], GetString method [Text Services Framework],ITfCandidateString interface, ITfCandidateString interface [Text Services Framework],GetString method, ITfCandidateString.GetString, ITfCandidateString::GetString, _tsf_itfcandidatestring_getstring_ref, ctffunc/ITfCandidateString::GetString, tsf.itfcandidatestring_getstring
ms.topic: method
f1_keywords: 
 - "ctffunc/ITfCandidateString.GetString"
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateString.GetString
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCandidateString::GetString


## -description




## -parameters




### -param pbstr [out]

Pointer to a <b>BSTR</b> value that receives the text of the candidate string object. The caller must release this memory using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstr</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatestring">ITfCandidateString</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>
 

 

