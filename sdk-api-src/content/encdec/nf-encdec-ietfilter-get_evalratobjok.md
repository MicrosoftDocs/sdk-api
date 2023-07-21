---
UID: NF:encdec.IETFilter.get_EvalRatObjOK
title: IETFilter::get_EvalRatObjOK (encdec.h)
description: .
helpviewer_keywords: ["IETFilter interface [Microsoft TV Technologies]","get_EvalRatObjOK method","IETFilter.get_EvalRatObjOK","IETFilter::get_EvalRatObjOK","IETFilterget_EvalRatObjOK","encdec/IETFilter::get_EvalRatObjOK","get_EvalRatObjOK","get_EvalRatObjOK method [Microsoft TV Technologies]","get_EvalRatObjOK method [Microsoft TV Technologies]","IETFilter interface","mstv.ietfilter_get_evalratobjok"]
old-location: mstv\ietfilter_get_evalratobjok.htm
tech.root: mstv
ms.assetid: ac76a634-af8d-4cf7-aab5-9022ce79ff31
ms.date: 12/05/2018
ms.keywords: IETFilter interface [Microsoft TV Technologies],get_EvalRatObjOK method, IETFilter.get_EvalRatObjOK, IETFilter::get_EvalRatObjOK, IETFilterget_EvalRatObjOK, encdec/IETFilter::get_EvalRatObjOK, get_EvalRatObjOK, get_EvalRatObjOK method [Microsoft TV Technologies], get_EvalRatObjOK method [Microsoft TV Technologies],IETFilter interface, mstv.ietfilter_get_evalratobjok
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
 - IETFilter::get_EvalRatObjOK
 - encdec/IETFilter::get_EvalRatObjOK
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
 - IETFilter.get_EvalRatObjOK
---

# IETFilter::get_EvalRatObjOK


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

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ietfilter">IETFilter Interface</a>