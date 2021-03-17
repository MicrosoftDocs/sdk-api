---
UID: NF:rend.ITDirectory.EnableAutoRefresh
title: ITDirectory::EnableAutoRefresh (rend.h)
description: The EnableAutoRefresh method enables auto refresh for directory objects created after it is called. Only applies to dynamic servers.
helpviewer_keywords: ["EnableAutoRefresh","EnableAutoRefresh method [TAPI 2.2]","EnableAutoRefresh method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","EnableAutoRefresh method","ITDirectory.EnableAutoRefresh","ITDirectory::EnableAutoRefresh","_tapi3_itdirectory_enableautorefresh","rend/ITDirectory::EnableAutoRefresh","tapi3.itdirectory_enableautorefresh"]
old-location: tapi3\itdirectory_enableautorefresh.htm
tech.root: tapi3
ms.assetid: f4d55d7c-54b4-44ee-b8f2-f4dd51bf823d
ms.date: 12/05/2018
ms.keywords: EnableAutoRefresh, EnableAutoRefresh method [TAPI 2.2], EnableAutoRefresh method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],EnableAutoRefresh method, ITDirectory.EnableAutoRefresh, ITDirectory::EnableAutoRefresh, _tapi3_itdirectory_enableautorefresh, rend/ITDirectory::EnableAutoRefresh, tapi3.itdirectory_enableautorefresh
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectory::EnableAutoRefresh
 - rend/ITDirectory::EnableAutoRefresh
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectory.EnableAutoRefresh
---

# ITDirectory::EnableAutoRefresh


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnableAutoRefresh</b> method enables auto refresh for directory objects created after it is called. Only applies to dynamic servers.

## -parameters

### -param fEnable [in]

Set to VARIANT_TRUE if auto refresh is to be enabled.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fEnable</i> parameter is not valid.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>