---
UID: NF:encdec.IDTFilter.get_BlockUnRatedDelay
title: IDTFilter::get_BlockUnRatedDelay (encdec.h)
description: The get_BlockUnRatedDelay method retrieves that length of time the filter waits before it blocks unrated content.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","get_BlockUnRatedDelay method","IDTFilter.get_BlockUnRatedDelay","IDTFilter::get_BlockUnRatedDelay","IDTFilterget_BlockUnRatedDelay","encdec/IDTFilter::get_BlockUnRatedDelay","get_BlockUnRatedDelay","get_BlockUnRatedDelay method [Microsoft TV Technologies]","get_BlockUnRatedDelay method [Microsoft TV Technologies]","IDTFilter interface","mstv.idtfilter_get_blockunrateddelay"]
old-location: mstv\idtfilter_get_blockunrateddelay.htm
tech.root: mstv
ms.assetid: 6852f376-35ab-4628-9068-51a2ca2ea31f
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_BlockUnRatedDelay method, IDTFilter.get_BlockUnRatedDelay, IDTFilter::get_BlockUnRatedDelay, IDTFilterget_BlockUnRatedDelay, encdec/IDTFilter::get_BlockUnRatedDelay, get_BlockUnRatedDelay, get_BlockUnRatedDelay method [Microsoft TV Technologies], get_BlockUnRatedDelay method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_blockunrateddelay
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDTFilter::get_BlockUnRatedDelay
 - encdec/IDTFilter::get_BlockUnRatedDelay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IDTFilter.get_BlockUnRatedDelay
---

# IDTFilter::get_BlockUnRatedDelay


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_BlockUnRatedDelay</b> method retrieves that length of time the filter waits before it blocks unrated content.

## -parameters

### -param pmsecsDelayBeforeBlock [out, retval]

Receives the delay, in milliseconds.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

Regardless of the value of this property, the filter does not block unrated content unless the <b>BlockUnRated</b> property is <b>TRUE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>



<a href="/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-get_blockunrated">IDTFilter::get_BlockUnRated</a>