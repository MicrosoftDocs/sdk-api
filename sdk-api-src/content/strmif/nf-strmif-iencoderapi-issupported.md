---
UID: NF:strmif.IEncoderAPI.IsSupported
title: IEncoderAPI::IsSupported (strmif.h)
description: The IsSupported method queries whether a given parameter is supported.
helpviewer_keywords: ["IEncoderAPI interface [Microsoft TV Technologies]","IsSupported method","IEncoderAPI.IsSupported","IEncoderAPI::IsSupported","IEncoderAPIIsSupported","IsSupported","IsSupported method [Microsoft TV Technologies]","IsSupported method [Microsoft TV Technologies]","IEncoderAPI interface","mstv.iencoderapi_issupported","strmif/IEncoderAPI::IsSupported"]
old-location: mstv\iencoderapi_issupported.htm
tech.root: mstv
ms.assetid: bbcbde18-2b2d-48b0-9f52-185648f502ce
ms.date: 12/05/2018
ms.keywords: IEncoderAPI interface [Microsoft TV Technologies],IsSupported method, IEncoderAPI.IsSupported, IEncoderAPI::IsSupported, IEncoderAPIIsSupported, IsSupported, IsSupported method [Microsoft TV Technologies], IsSupported method [Microsoft TV Technologies],IEncoderAPI interface, mstv.iencoderapi_issupported, strmif/IEncoderAPI::IsSupported
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEncoderAPI::IsSupported
 - strmif/IEncoderAPI::IsSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEncoderAPI.IsSupported
---

# IEncoderAPI::IsSupported


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> is no longer available for use. Instead, use <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>IsSupported</b> method queries whether a given parameter is supported.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the parameter.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The encoder supports the parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The encoder does not support the parameter.

</td>
</tr>
</table>

## -remarks

The method returns S_OK if the encoder recognizes the GUID. To check whether the parameter can be read or modified, call the <a href="/windows/desktop/api/strmif/nf-strmif-iencoderapi-isavailable">IEncoderAPI::IsAvailable</a> method.
      

Any errors besides those in the table above indicate an inability to process the call.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI Interface</a>