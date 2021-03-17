---
UID: NF:tapi3if.ITMultiTrackTerminal.get_TrackTerminals
title: ITMultiTrackTerminal::get_TrackTerminals (tapi3if.h)
description: The get_TrackTerminals method creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called.
helpviewer_keywords: ["ITMultiTrackTerminal interface [TAPI 2.2]","get_TrackTerminals method","ITMultiTrackTerminal.get_TrackTerminals","ITMultiTrackTerminal::get_TrackTerminals","_tapi3_itmultitrackterminal_get_trackterminals","get_TrackTerminals","get_TrackTerminals method [TAPI 2.2]","get_TrackTerminals method [TAPI 2.2]","ITMultiTrackTerminal interface","tapi3.itmultitrackterminal_get_trackterminals","tapi3if/ITMultiTrackTerminal::get_TrackTerminals"]
old-location: tapi3\itmultitrackterminal_get_trackterminals.htm
tech.root: tapi3
ms.assetid: 2bedefe8-6b84-48c0-8a7b-719d017baf24
ms.date: 12/05/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_TrackTerminals method, ITMultiTrackTerminal.get_TrackTerminals, ITMultiTrackTerminal::get_TrackTerminals, _tapi3_itmultitrackterminal_get_trackterminals, get_TrackTerminals, get_TrackTerminals method [TAPI 2.2], get_TrackTerminals method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_trackterminals, tapi3if/ITMultiTrackTerminal::get_TrackTerminals
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
 - ITMultiTrackTerminal::get_TrackTerminals
 - tapi3if/ITMultiTrackTerminal::get_TrackTerminals
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
 - ITMultiTrackTerminal.get_TrackTerminals
---

# ITMultiTrackTerminal::get_TrackTerminals


## -description

The 
<b>get_TrackTerminals</b> method creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called. The variant returned contains a pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> interface that can be used to iterate through elements of type 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>. The elements of the collection contain pointers to tracks.

## -parameters

### -param pVariant [out]

Pointer to a VARIANT containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointers for the tracks available.

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
The <i>pVariant</i> parameter is not a valid pointer.

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
The <i>pVariant</i> parameter was not empty.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITMultiTrackTerminal::get_TrackTerminals</b>. The application must call <b>Release</b> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal">ITMultiTrackTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>