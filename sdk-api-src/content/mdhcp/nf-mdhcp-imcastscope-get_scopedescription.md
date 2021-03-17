---
UID: NF:mdhcp.IMcastScope.get_ScopeDescription
title: IMcastScope::get_ScopeDescription (mdhcp.h)
description: The get_ScopeDescription method obtains a textual description associated with this scope. The description is used only for clarifying the purpose or meaning of a scope and is not needed for any subsequent calls.
helpviewer_keywords: ["IMcastScope interface [TAPI 2.2]","get_ScopeDescription method","IMcastScope.get_ScopeDescription","IMcastScope::get_ScopeDescription","_tapi3_imcastscope_get_scopedescription","get_ScopeDescription","get_ScopeDescription method [TAPI 2.2]","get_ScopeDescription method [TAPI 2.2]","IMcastScope interface","mdhcp/IMcastScope::get_ScopeDescription","tapi3.imcastscope_get_scopedescription"]
old-location: tapi3\imcastscope_get_scopedescription.htm
tech.root: tapi3
ms.assetid: e675ba4a-8e5f-42a6-8edf-9b136cf9dd46
ms.date: 12/05/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_ScopeDescription method, IMcastScope.get_ScopeDescription, IMcastScope::get_ScopeDescription, _tapi3_imcastscope_get_scopedescription, get_ScopeDescription, get_ScopeDescription method [TAPI 2.2], get_ScopeDescription method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_ScopeDescription, tapi3.imcastscope_get_scopedescription
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
 - IMcastScope::get_ScopeDescription
 - mdhcp/IMcastScope::get_ScopeDescription
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
 - IMcastScope.get_ScopeDescription
---

# IMcastScope::get_ScopeDescription


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_ScopeDescription</b> method obtains a textual description associated with this scope. The description is used only for clarifying the purpose or meaning of a scope and is not needed for any subsequent calls.

## -parameters

### -param ppDescription [out]

Pointer to a <b>BSTR</b> that will receive a description of this scope. The description was established when this scope was configured on the multicast server.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to allocate the string.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDescription</i> parameter.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>