---
UID: NN:mfidl.IMFMediaSourceEx
title: IMFMediaSourceEx (mfidl.h)
description: Extends the IMFMediaSource interface to provide additional capabilities for a media source.
helpviewer_keywords: ["IMFMediaSourceEx","IMFMediaSourceEx interface [Media Foundation]","IMFMediaSourceEx interface [Media Foundation]","described","mf.imfmediasourceex","mfidl/IMFMediaSourceEx"]
old-location: mf\imfmediasourceex.htm
tech.root: mf
ms.assetid: C72C79D5-FD65-4F27-A8C8-B94BF5A9E829
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceEx, IMFMediaSourceEx interface [Media Foundation], IMFMediaSourceEx interface [Media Foundation],described, mf.imfmediasourceex, mfidl/IMFMediaSourceEx
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaSourceEx
 - mfidl/IMFMediaSourceEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFMediaSourceEx
---

# IMFMediaSourceEx interface


## -description

Extends the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface to provide additional capabilities for a media source.

To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the media source.

## -inheritance

The <b>IMFMediaSourceEx</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>. <b>IMFMediaSourceEx</b> also has these types of members:

## -remarks

Implementations of this interface can return <b>E_NOTIMPL</b> for any methods that are not required by the media source.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
