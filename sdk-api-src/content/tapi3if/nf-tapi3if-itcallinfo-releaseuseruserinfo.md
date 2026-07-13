---
UID: NF:tapi3if.ITCallInfo.ReleaseUserUserInfo
title: ITCallInfo::ReleaseUserUserInfo (tapi3if.h)
description: The ReleaseUserUserInfo method informs the service provider that the application has processed the user-user information obtained from the ITCallInfo::GetCallInfoBuffer method.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","ReleaseUserUserInfo method","ITCallInfo.ReleaseUserUserInfo","ITCallInfo::ReleaseUserUserInfo","ReleaseUserUserInfo","ReleaseUserUserInfo method [TAPI 2.2]","ReleaseUserUserInfo method [TAPI 2.2]","ITCallInfo interface","_tapi3_itcallinfo_releaseuseruserinfo","tapi3.itcallinfo_releaseuseruserinfo","tapi3if/ITCallInfo::ReleaseUserUserInfo"]
old-location: tapi3\itcallinfo_releaseuseruserinfo.htm
tech.root: tapi3
ms.assetid: 019823a3-e70d-4b0c-b996-07a13f2bd5f3
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],ReleaseUserUserInfo method, ITCallInfo.ReleaseUserUserInfo, ITCallInfo::ReleaseUserUserInfo, ReleaseUserUserInfo, ReleaseUserUserInfo method [TAPI 2.2], ReleaseUserUserInfo method [TAPI 2.2],ITCallInfo interface, _tapi3_itcallinfo_releaseuseruserinfo, tapi3.itcallinfo_releaseuseruserinfo, tapi3if/ITCallInfo::ReleaseUserUserInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCallInfo::ReleaseUserUserInfo
 - tapi3if/ITCallInfo::ReleaseUserUserInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo.ReleaseUserUserInfo
---

# ITCallInfo::ReleaseUserUserInfo


## -description

The 
<b>ReleaseUserUserInfo</b> method informs the service provider that the application has processed the user-user information obtained from the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">ITCallInfo::GetCallInfoBuffer</a> method, called with the CIB_USERUSERINFO member of 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a>, and subsequently received user-user information can now be written.



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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>
