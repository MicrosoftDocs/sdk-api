---
UID: NF:encdec.IDTFilter.get_BlockUnRated
title: IDTFilter::get_BlockUnRated (encdec.h)
description: The get_BlockUnRated method indicates whether a program without rating information is blocked.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","get_BlockUnRated method","IDTFilter.get_BlockUnRated","IDTFilter::get_BlockUnRated","IDTFilterget_BlockUnRated","encdec/IDTFilter::get_BlockUnRated","get_BlockUnRated","get_BlockUnRated method [Microsoft TV Technologies]","get_BlockUnRated method [Microsoft TV Technologies]","IDTFilter interface","mstv.idtfilter_get_blockunrated"]
old-location: mstv\idtfilter_get_blockunrated.htm
tech.root: mstv
ms.assetid: 9b8ecc6b-02e8-47e9-a8df-6e73d58dd177
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_BlockUnRated method, IDTFilter.get_BlockUnRated, IDTFilter::get_BlockUnRated, IDTFilterget_BlockUnRated, encdec/IDTFilter::get_BlockUnRated, get_BlockUnRated, get_BlockUnRated method [Microsoft TV Technologies], get_BlockUnRated method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_blockunrated
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
 - IDTFilter::get_BlockUnRated
 - encdec/IDTFilter::get_BlockUnRated
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
 - IDTFilter.get_BlockUnRated
---

# IDTFilter::get_BlockUnRated


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_BlockUnRated</b> method indicates whether a program without rating information is blocked.

## -parameters

### -param pfBlockUnRatedShows [out, retval]

Receives a Boolean value. If the value is <b>TRUE</b>, unrated shows are blocked. Otherwise, they are not blocked.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <b>EvalRat</b> object was not successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-get_blockunrated">IEvalRat::get_BlockUnRated</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>