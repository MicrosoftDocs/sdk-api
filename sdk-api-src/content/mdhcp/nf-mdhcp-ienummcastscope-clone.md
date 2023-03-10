---
UID: NF:mdhcp.IEnumMcastScope.Clone
title: IEnumMcastScope::Clone (mdhcp.h)
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. (IEnumMcastScope.Clone)
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumMcastScope interface","IEnumMcastScope interface [TAPI 2.2]","Clone method","IEnumMcastScope.Clone","IEnumMcastScope::Clone","_tapi3_ienummcastscope_clone","mdhcp/IEnumMcastScope::Clone","tapi3.ienummcastscope_clone"]
old-location: tapi3\ienummcastscope_clone.htm
tech.root: tapi3
ms.assetid: 96b2a09f-8a02-471d-a738-f81a8132e0c1
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumMcastScope interface, IEnumMcastScope interface [TAPI 2.2],Clone method, IEnumMcastScope.Clone, IEnumMcastScope::Clone, _tapi3_ienummcastscope_clone, mdhcp/IEnumMcastScope::Clone, tapi3.ienummcastscope_clone
req.header: mdhcp.h
req.include-header: 
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
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumMcastScope::Clone
 - mdhcp/IEnumMcastScope::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IEnumMcastScope.Clone
---

# IEnumMcastScope::Clone


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppEnum [out]

Pointer to the new 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a> object.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a> interface returned by <b>IEnumMcastScope::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumMcastScope</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a>
