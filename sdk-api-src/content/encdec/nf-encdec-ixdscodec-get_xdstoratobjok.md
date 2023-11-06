---
UID: NF:encdec.IXDSCodec.get_XDSToRatObjOK
title: IXDSCodec::get_XDSToRatObjOK (encdec.h)
description: The get_XDSToRatObjOK method queries whether the XDSToRat object was created successfully.
helpviewer_keywords: ["IXDSCodec interface [Microsoft TV Technologies]","get_XDSToRatObjOK method","IXDSCodec.get_XDSToRatObjOK","IXDSCodec::get_XDSToRatObjOK","IXDSCodecXDSToRatObjOK","encdec/IXDSCodec::get_XDSToRatObjOK","get_XDSToRatObjOK","get_XDSToRatObjOK method [Microsoft TV Technologies]","get_XDSToRatObjOK method [Microsoft TV Technologies]","IXDSCodec interface","mstv.ixdscodec_get_xdstoratobjok"]
old-location: mstv\ixdscodec_get_xdstoratobjok.htm
tech.root: mstv
ms.assetid: 846f3f68-8745-416d-9f0e-1e6ef83054b2
ms.date: 12/05/2018
ms.keywords: IXDSCodec interface [Microsoft TV Technologies],get_XDSToRatObjOK method, IXDSCodec.get_XDSToRatObjOK, IXDSCodec::get_XDSToRatObjOK, IXDSCodecXDSToRatObjOK, encdec/IXDSCodec::get_XDSToRatObjOK, get_XDSToRatObjOK, get_XDSToRatObjOK method [Microsoft TV Technologies], get_XDSToRatObjOK method [Microsoft TV Technologies],IXDSCodec interface, mstv.ixdscodec_get_xdstoratobjok
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
 - IXDSCodec::get_XDSToRatObjOK
 - encdec/IXDSCodec::get_XDSToRatObjOK
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
 - IXDSCodec.get_XDSToRatObjOK
---

# IXDSCodec::get_XDSToRatObjOK


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_XDSToRatObjOK</b> method queries whether the <b>XDSToRat</b> object was created successfully.

## -parameters

### -param pHrCoCreateRetVal [out, retval]

Receives an <b>HRESULT</b> value. The <b>HRESULT</b> is the value that was returned when the filter called <b>CoCreateInstance</b> to create the <b>XDSToRat</b> object. If it equals S_OK, the <b>EvalRat</b> object was created successfully.

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

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodec">IXDSCodec Interface</a>