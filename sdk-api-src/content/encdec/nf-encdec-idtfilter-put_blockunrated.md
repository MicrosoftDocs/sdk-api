---
UID: NF:encdec.IDTFilter.put_BlockUnRated
title: IDTFilter::put_BlockUnRated (encdec.h)
description: The put_BlockUnRated method specifies whether to block a program for which rating information has not been obtained.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","put_BlockUnRated method","IDTFilter.put_BlockUnRated","IDTFilter::put_BlockUnRated","IDTFilterput_BlockUnRated","encdec/IDTFilter::put_BlockUnRated","mstv.idtfilter_put_blockunrated","put_BlockUnRated","put_BlockUnRated method [Microsoft TV Technologies]","put_BlockUnRated method [Microsoft TV Technologies]","IDTFilter interface"]
old-location: mstv\idtfilter_put_blockunrated.htm
tech.root: mstv
ms.assetid: 2b6ef516-bbc8-4d17-a306-433e8265e879
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],put_BlockUnRated method, IDTFilter.put_BlockUnRated, IDTFilter::put_BlockUnRated, IDTFilterput_BlockUnRated, encdec/IDTFilter::put_BlockUnRated, mstv.idtfilter_put_blockunrated, put_BlockUnRated, put_BlockUnRated method [Microsoft TV Technologies], put_BlockUnRated method [Microsoft TV Technologies],IDTFilter interface
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
 - IDTFilter::put_BlockUnRated
 - encdec/IDTFilter::put_BlockUnRated
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
 - IDTFilter.put_BlockUnRated
---

# IDTFilter::put_BlockUnRated


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_BlockUnRated</b> method specifies whether to block a program for which rating information has not been obtained.

## -parameters

### -param fBlockUnRatedShows [in]

Boolean value. Specify <b>TRUE</b> to block unrated programs, or specify <b>FALSE</b> not to block unrated programs.

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

The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockunrated">IEvalRat::put_BlockUnRated</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>