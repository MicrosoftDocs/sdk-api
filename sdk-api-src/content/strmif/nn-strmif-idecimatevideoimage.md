---
UID: NN:strmif.IDecimateVideoImage
title: IDecimateVideoImage (strmif.h)
description: The IDecimateVideoImage interface specifies decimation on a decoder filter.
helpviewer_keywords: ["IDecimateVideoImage","IDecimateVideoImage interface [DirectShow]","IDecimateVideoImage interface [DirectShow]","described","IDecimateVideoImageInterface","dshow.idecimatevideoimage","strmif/IDecimateVideoImage"]
old-location: dshow\idecimatevideoimage.htm
tech.root: dshow
ms.assetid: 0d338d41-546f-41da-bc1f-b1dd74b399ef
ms.date: 12/05/2018
ms.keywords: IDecimateVideoImage, IDecimateVideoImage interface [DirectShow], IDecimateVideoImage interface [DirectShow],described, IDecimateVideoImageInterface, dshow.idecimatevideoimage, strmif/IDecimateVideoImage
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDecimateVideoImage
 - strmif/IDecimateVideoImage
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
 - IDecimateVideoImage
---

# IDecimateVideoImage interface


## -description

The <code>IDecimateVideoImage</code> interface specifies decimation on a decoder filter. The term <i>decimation</i> refers to scaling the video output down to a size smaller than the native size of the video.

Applications must not call methods on this interface. The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter uses this interface to decimate video at the video decoder.

Decoder filters that can decimate their video output should support this interface.

## -inheritance

The <b>IDecimateVideoImage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDecimateVideoImage</b> also has these types of members:

