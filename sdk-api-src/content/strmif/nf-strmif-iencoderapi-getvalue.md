---
UID: NF:strmif.IEncoderAPI.GetValue
title: IEncoderAPI::GetValue (strmif.h)
description: The GetValue method retrieves the current value of a specified parameter.
helpviewer_keywords: ["GetValue","GetValue method [Microsoft TV Technologies]","GetValue method [Microsoft TV Technologies]","IEncoderAPI interface","IEncoderAPI interface [Microsoft TV Technologies]","GetValue method","IEncoderAPI.GetValue","IEncoderAPI::GetValue","IEncoderAPIGetValue","mstv.iencoderapi_getvalue","strmif/IEncoderAPI::GetValue"]
old-location: mstv\iencoderapi_getvalue.htm
tech.root: mstv
ms.assetid: 62f69677-05cd-46ab-8b77-96e10f8fbb1d
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Microsoft TV Technologies], GetValue method [Microsoft TV Technologies],IEncoderAPI interface, IEncoderAPI interface [Microsoft TV Technologies],GetValue method, IEncoderAPI.GetValue, IEncoderAPI::GetValue, IEncoderAPIGetValue, mstv.iencoderapi_getvalue, strmif/IEncoderAPI::GetValue
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
 - IEncoderAPI::GetValue
 - strmif/IEncoderAPI::GetValue
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
 - IEncoderAPI.GetValue
---

# IEncoderAPI::GetValue


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> is no longer available for use. Instead, use <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>GetValue</b> method retrieves the current value of a specified parameter.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the parameter.

### -param Value [out]

Receives the value for the parameter specified in <i>Api</i>. If <i>Api</i> was specified as ENCAPIPARAM_BITRATE_MODE, then <i>Value</i> will be one of the <a href="/windows/desktop/api/strmif/ne-strmif-videoencoder_bitrate_mode">VIDEOENCODER_BITRATE_MODE</a> constants.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI Interface</a>