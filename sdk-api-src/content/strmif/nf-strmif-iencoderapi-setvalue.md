---
UID: NF:strmif.IEncoderAPI.SetValue
title: IEncoderAPI::SetValue (strmif.h)
description: The SetValue method sets the current value of a parameter.
helpviewer_keywords: ["IEncoderAPI interface [Microsoft TV Technologies]","SetValue method","IEncoderAPI.SetValue","IEncoderAPI::SetValue","IEncoderAPISetValue","SetValue","SetValue method [Microsoft TV Technologies]","SetValue method [Microsoft TV Technologies]","IEncoderAPI interface","mstv.iencoderapi_setvalue","strmif/IEncoderAPI::SetValue"]
old-location: mstv\iencoderapi_setvalue.htm
tech.root: mstv
ms.assetid: a7dc0964-64b9-4ea3-8948-19ec100d64f5
ms.date: 12/05/2018
ms.keywords: IEncoderAPI interface [Microsoft TV Technologies],SetValue method, IEncoderAPI.SetValue, IEncoderAPI::SetValue, IEncoderAPISetValue, SetValue, SetValue method [Microsoft TV Technologies], SetValue method [Microsoft TV Technologies],IEncoderAPI interface, mstv.iencoderapi_setvalue, strmif/IEncoderAPI::SetValue
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
 - IEncoderAPI::SetValue
 - strmif/IEncoderAPI::SetValue
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
 - IEncoderAPI.SetValue
---

# IEncoderAPI::SetValue


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> is no longer available for use. Instead, use <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>SetValue</b> method sets the current value of a parameter.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the parameter.

### -param Value [out]

Pointer that specifies the value of <i>Api</i>. If <i>Api</i> was specified as <b>ENCAPIPARAM_BITRATE_MODE</b>, then <i>Value</i> must be one of the <a href="/windows/desktop/api/strmif/ne-strmif-videoencoder_bitrate_mode">VIDEOENCODER_BITRATE_MODE</a> constants.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI Interface</a>