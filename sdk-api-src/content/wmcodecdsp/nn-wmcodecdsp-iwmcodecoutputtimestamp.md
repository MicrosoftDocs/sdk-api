---
UID: NN:wmcodecdsp.IWMCodecOutputTimestamp
title: IWMCodecOutputTimestamp (wmcodecdsp.h)
description: Gets the time stamp of the next video frame to be decoded.
helpviewer_keywords: ["IWMCodecOutputTimestamp","IWMCodecOutputTimestamp interface [Media Foundation]","IWMCodecOutputTimestamp interface [Media Foundation]","described","codecapi.iwmcodecoutputtimestampinterface","mf.iwmcodecoutputtimestampinterface","wmcodecdsp/IWMCodecOutputTimestamp"]
old-location: mf\iwmcodecoutputtimestampinterface.htm
tech.root: mf
ms.assetid: 0dbac3fa-7521-434d-aa0a-2e8422c3da59
ms.date: 12/05/2018
ms.keywords: IWMCodecOutputTimestamp, IWMCodecOutputTimestamp interface [Media Foundation], IWMCodecOutputTimestamp interface [Media Foundation],described, codecapi.iwmcodecoutputtimestampinterface, mf.iwmcodecoutputtimestampinterface, wmcodecdsp/IWMCodecOutputTimestamp
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMCodecOutputTimestamp
 - wmcodecdsp/IWMCodecOutputTimestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecOutputTimestamp
---

# IWMCodecOutputTimestamp interface


## -description

Gets the time stamp of the  next video frame to be decoded.

This interface is implemented by the video decoders. You can obtain a pointer to <b>IWMCodecOutputTimestamp</b> by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of any other interface of the decoder object, such as <a href="/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>.

## -inheritance

The <b>IWMCodecOutputTimestamp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecOutputTimestamp</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/configuringvideodecoding">Configuring Video Decoding</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
