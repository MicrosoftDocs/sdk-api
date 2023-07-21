---
UID: NF:strmif.IEncoderAPI.IsAvailable
title: IEncoderAPI::IsAvailable (strmif.h)
description: IEncoderAPI is no longer available for use. (IEncoderAPI.IsAvailable)
helpviewer_keywords: ["IEncoderAPI interface [Microsoft TV Technologies]","IsAvailable method","IEncoderAPI.IsAvailable","IEncoderAPI::IsAvailable","IEncoderAPIIsAvailable","IsAvailable","IsAvailable method [Microsoft TV Technologies]","IsAvailable method [Microsoft TV Technologies]","IEncoderAPI interface","mstv.iencoderapi_isavailable","strmif/IEncoderAPI::IsAvailable"]
old-location: mstv\iencoderapi_isavailable.htm
tech.root: mstv
ms.assetid: ad94b70f-fd35-44b4-8322-9891cd7f17cc
ms.date: 12/05/2018
ms.keywords: IEncoderAPI interface [Microsoft TV Technologies],IsAvailable method, IEncoderAPI.IsAvailable, IEncoderAPI::IsAvailable, IEncoderAPIIsAvailable, IsAvailable, IsAvailable method [Microsoft TV Technologies], IsAvailable method [Microsoft TV Technologies],IEncoderAPI interface, mstv.iencoderapi_isavailable, strmif/IEncoderAPI::IsAvailable
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
 - IEncoderAPI::IsAvailable
 - strmif/IEncoderAPI::IsAvailable
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
 - IEncoderAPI.IsAvailable
---

# IEncoderAPI::IsAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> is no longer available for use. Instead, use <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>IsAvailable</b> method queries whether a given parameter can be read and modified.

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
The parameter can be read and modified. (Set and get operations are supported for this parameter.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The parameter cannot be read or modified.

</td>
</tr>
</table>

## -remarks

Any errors besides those in the table above indicate an inability to process the call.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI Interface</a>
