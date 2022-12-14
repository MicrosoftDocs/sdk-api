---
UID: NF:mdhcp.IEnumMcastScope.Next
title: IEnumMcastScope::Next (mdhcp.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. (IEnumMcastScope.Next)
helpviewer_keywords: ["IEnumMcastScope interface [TAPI 2.2]","Next method","IEnumMcastScope.Next","IEnumMcastScope::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumMcastScope interface","_tapi3_ienummcastscope_next","mdhcp/IEnumMcastScope::Next","tapi3.ienummcastscope_next"]
old-location: tapi3\ienummcastscope_next.htm
tech.root: tapi3
ms.assetid: f7618414-c2fc-46c8-8f9d-c1ad217c8d94
ms.date: 12/05/2018
ms.keywords: IEnumMcastScope interface [TAPI 2.2],Next method, IEnumMcastScope.Next, IEnumMcastScope::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumMcastScope interface, _tapi3_ienummcastscope_next, mdhcp/IEnumMcastScope::Next, tapi3.ienummcastscope_next
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
 - IEnumMcastScope::Next
 - mdhcp/IEnumMcastScope::Next
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
 - IEnumMcastScope.Next
---

# IEnumMcastScope::Next


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppScopes [out]

Pointer to the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface.

### -param pceltFetched [out]

Pointer to the number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppScopes</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface returned by <b>IEnumMcastScope::Next</b>. The application must call <b>Release</b> on the 
<b>IMcastScope</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a>
