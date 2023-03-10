---
UID: NF:strmif.IAMAnalogVideoEncoder.get_TVFormat
title: IAMAnalogVideoEncoder::get_TVFormat (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_TVFormat method retrieves the analog video standard that the encoder is currently set to (NTSC/M, PAL/B, SECAM/K1, and so on).
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","get_TVFormat method","IAMAnalogVideoEncoder.get_TVFormat","IAMAnalogVideoEncoder::get_TVFormat","IAMAnalogVideoEncoderget_TVFormat","dshow.iamanalogvideoencoder_get_tvformat","get_TVFormat","get_TVFormat method [DirectShow]","get_TVFormat method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::get_TVFormat"]
old-location: dshow\iamanalogvideoencoder_get_tvformat.htm
tech.root: dshow
ms.assetid: 5a88e2e7-508b-448b-ac1d-50a50b4bb79a
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_TVFormat method, IAMAnalogVideoEncoder.get_TVFormat, IAMAnalogVideoEncoder::get_TVFormat, IAMAnalogVideoEncoderget_TVFormat, dshow.iamanalogvideoencoder_get_tvformat, get_TVFormat, get_TVFormat method [DirectShow], get_TVFormat method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_TVFormat
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAnalogVideoEncoder::get_TVFormat
 - strmif/IAMAnalogVideoEncoder::get_TVFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.get_TVFormat
---

# IAMAnalogVideoEncoder::get_TVFormat


## -description

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_TVFormat</code> method retrieves the analog video standard that the encoder is currently set to (NTSC/M, PAL/B, SECAM/K1, and so on).

## -parameters

### -param plAnalogVideoStandard [out]

Specifies a pointer to a <b>long</b> integer to receive the encoder's current video standard.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Possible values and their meaning are defined in the [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>