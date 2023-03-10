---
UID: NF:strmif.IAMAnalogVideoEncoder.put_CopyProtection
title: IAMAnalogVideoEncoder::put_CopyProtection (strmif.h)
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_CopyProtection method sets the level of copy protection for the encoder.
helpviewer_keywords: ["IAMAnalogVideoEncoder interface [DirectShow]","put_CopyProtection method","IAMAnalogVideoEncoder.put_CopyProtection","IAMAnalogVideoEncoder::put_CopyProtection","IAMAnalogVideoEncoderput_CopyProtection","dshow.iamanalogvideoencoder_put_copyprotection","put_CopyProtection","put_CopyProtection method [DirectShow]","put_CopyProtection method [DirectShow]","IAMAnalogVideoEncoder interface","strmif/IAMAnalogVideoEncoder::put_CopyProtection"]
old-location: dshow\iamanalogvideoencoder_put_copyprotection.htm
tech.root: dshow
ms.assetid: a2a762f3-8b11-4334-979d-206234d6cf09
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_CopyProtection method, IAMAnalogVideoEncoder.put_CopyProtection, IAMAnalogVideoEncoder::put_CopyProtection, IAMAnalogVideoEncoderput_CopyProtection, dshow.iamanalogvideoencoder_put_copyprotection, put_CopyProtection, put_CopyProtection method [DirectShow], put_CopyProtection method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_CopyProtection
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
 - IAMAnalogVideoEncoder::put_CopyProtection
 - strmif/IAMAnalogVideoEncoder::put_CopyProtection
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
 - IAMAnalogVideoEncoder.put_CopyProtection
---

# IAMAnalogVideoEncoder::put_CopyProtection


## -description

<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_CopyProtection</code> method sets the level of copy protection for the encoder.

## -parameters

### -param lVideoCopyProtection [in]

Specifies the level of copy protection as a <b>long</b> integer with a value as defined in the <a href="/previous-versions/ms778997(v=vs.85)">AM_COPY_MACROVISION_LEVEL</a> enumeration.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamanalogvideoencoder">IAMAnalogVideoEncoder Interface</a>