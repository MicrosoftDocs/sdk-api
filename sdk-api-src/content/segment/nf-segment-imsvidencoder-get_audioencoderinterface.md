---
UID: NF:segment.IMSVidEncoder.get_AudioEncoderInterface
title: IMSVidEncoder::get_AudioEncoderInterface (segment.h)
description: The get_AudioEncoderInterface method retrieves a pointer to the audio encoder interface.
helpviewer_keywords: ["IMSVidEncoder interface [Microsoft TV Technologies]","get_AudioEncoderInterface method","IMSVidEncoder.get_AudioEncoderInterface","IMSVidEncoder::get_AudioEncoderInterface","IMSVidEncoderget_AudioEncoderInterface","get_AudioEncoderInterface","get_AudioEncoderInterface method [Microsoft TV Technologies]","get_AudioEncoderInterface method [Microsoft TV Technologies]","IMSVidEncoder interface","mstv.imsvidencoder_get_audioencoderinterface","segment/IMSVidEncoder::get_AudioEncoderInterface"]
old-location: mstv\imsvidencoder_get_audioencoderinterface.htm
tech.root: mstv
ms.assetid: 5b22a062-7da5-411e-ac85-fb9c7b3650a7
ms.date: 12/05/2018
ms.keywords: IMSVidEncoder interface [Microsoft TV Technologies],get_AudioEncoderInterface method, IMSVidEncoder.get_AudioEncoderInterface, IMSVidEncoder::get_AudioEncoderInterface, IMSVidEncoderget_AudioEncoderInterface, get_AudioEncoderInterface, get_AudioEncoderInterface method [Microsoft TV Technologies], get_AudioEncoderInterface method [Microsoft TV Technologies],IMSVidEncoder interface, mstv.imsvidencoder_get_audioencoderinterface, segment/IMSVidEncoder::get_AudioEncoderInterface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidEncoder::get_AudioEncoderInterface
 - segment/IMSVidEncoder::get_AudioEncoderInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidEncoder.get_AudioEncoderInterface
---

# IMSVidEncoder::get_AudioEncoderInterface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AudioEncoderInterface</b> method retrieves a pointer to the audio encoder interface.

## -parameters

### -param ppEncInt [out]

Pointer to a variable that receives an <b>IUnknown</b> interface pointer. The caller can query this interface for the <a href="/windows/desktop/api/strmif/nn-strmif-iencoderapi">IEncoderAPI</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the method succeeds, the caller must release the <b>IUnknown</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidencoder">IMSVidEncoder Interface</a>