---
UID: NF:encdec.IDTFilter.get_EvalRatObjOK
title: IDTFilter::get_EvalRatObjOK (encdec.h)
description: The get_EvalRatObjOK method queries whether the EvalRat object was created successfully.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","get_EvalRatObjOK method","IDTFilter.get_EvalRatObjOK","IDTFilter::get_EvalRatObjOK","IDTFilterget_EvalRatObjOK","encdec/IDTFilter::get_EvalRatObjOK","get_EvalRatObjOK","get_EvalRatObjOK method [Microsoft TV Technologies]","get_EvalRatObjOK method [Microsoft TV Technologies]","IDTFilter interface","mstv.idtfilter_get_evalratobjok"]
old-location: mstv\idtfilter_get_evalratobjok.htm
tech.root: mstv
ms.assetid: 92bbe476-3aba-4a50-9cb3-500356228c4b
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_EvalRatObjOK method, IDTFilter.get_EvalRatObjOK, IDTFilter::get_EvalRatObjOK, IDTFilterget_EvalRatObjOK, encdec/IDTFilter::get_EvalRatObjOK, get_EvalRatObjOK, get_EvalRatObjOK method [Microsoft TV Technologies], get_EvalRatObjOK method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_evalratobjok
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
 - IDTFilter::get_EvalRatObjOK
 - encdec/IDTFilter::get_EvalRatObjOK
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
 - IDTFilter.get_EvalRatObjOK
---

# IDTFilter::get_EvalRatObjOK


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_EvalRatObjOK</b> method queries whether the <b>EvalRat</b> object was created successfully.

## -parameters

### -param pHrCoCreateRetVal [out, retval]

Receives an <b>HRESULT</b> value. The <b>HRESULT</b> is the value that was returned when the filter called <b>CoCreateInstance</b> to create the <b>EvalRat</b> object. If it equals S_OK, the <b>EvalRat</b> object was created successfully.

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
NULL pointer argument

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

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>