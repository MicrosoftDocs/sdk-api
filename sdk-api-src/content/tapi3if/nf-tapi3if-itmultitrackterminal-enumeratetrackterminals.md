---
UID: NF:tapi3if.ITMultiTrackTerminal.EnumerateTrackTerminals
title: ITMultiTrackTerminal::EnumerateTrackTerminals (tapi3if.h)
description: The EnumerateTrackTerminals method creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.
helpviewer_keywords: ["EnumerateTrackTerminals","EnumerateTrackTerminals method [TAPI 2.2]","EnumerateTrackTerminals method [TAPI 2.2]","ITMultiTrackTerminal interface","ITMultiTrackTerminal interface [TAPI 2.2]","EnumerateTrackTerminals method","ITMultiTrackTerminal.EnumerateTrackTerminals","ITMultiTrackTerminal::EnumerateTrackTerminals","_tapi3_itmultitrackterminal_enumeratetrackterminals","tapi3.itmultitrackterminal_enumeratetrackterminals","tapi3if/ITMultiTrackTerminal::EnumerateTrackTerminals"]
old-location: tapi3\itmultitrackterminal_enumeratetrackterminals.htm
tech.root: tapi3
ms.assetid: 90ef12f5-1a94-49ca-85c3-092306503827
ms.date: 12/05/2018
ms.keywords: EnumerateTrackTerminals, EnumerateTrackTerminals method [TAPI 2.2], EnumerateTrackTerminals method [TAPI 2.2],ITMultiTrackTerminal interface, ITMultiTrackTerminal interface [TAPI 2.2],EnumerateTrackTerminals method, ITMultiTrackTerminal.EnumerateTrackTerminals, ITMultiTrackTerminal::EnumerateTrackTerminals, _tapi3_itmultitrackterminal_enumeratetrackterminals, tapi3.itmultitrackterminal_enumeratetrackterminals, tapi3if/ITMultiTrackTerminal::EnumerateTrackTerminals
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
 - ITMultiTrackTerminal::EnumerateTrackTerminals
 - tapi3if/ITMultiTrackTerminal::EnumerateTrackTerminals
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
 - ITMultiTrackTerminal.EnumerateTrackTerminals
---

# ITMultiTrackTerminal::EnumerateTrackTerminals


## -description

The 
<b>EnumerateTrackTerminals</b> method creates and returns an enumeration containing the terminals contained by the multitrack terminal on which this method was called.

## -parameters

### -param ppEnumTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface enumerating terminals contained in the multitrack terminal.

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
The <i>ppTerminalEnum</i> parameter is not a valid pointer.

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
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface returned by <b>ITMultiTrackTerminal::EnumerateTrackTerminals</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal">ITMultiTrackTerminal</a>