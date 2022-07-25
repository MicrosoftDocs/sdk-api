---
UID: NN:wmcodecdsp.IWMCodecLeakyBucket
title: IWMCodecLeakyBucket (wmcodecdsp.h)
description: Configures the &quot;leaky bucket&quot; parameters on a video encoder.
helpviewer_keywords: ["IWMCodecLeakyBucket","IWMCodecLeakyBucket interface [Media Foundation]","IWMCodecLeakyBucket interface [Media Foundation]","described","codecapi.iwmcodecleakybucketinterface","mf.iwmcodecleakybucketinterface","wmcodecdsp/IWMCodecLeakyBucket"]
old-location: mf\iwmcodecleakybucketinterface.htm
tech.root: mf
ms.assetid: 93a0169e-39fe-4152-8698-72a0650be41a
ms.date: 12/05/2018
ms.keywords: IWMCodecLeakyBucket, IWMCodecLeakyBucket interface [Media Foundation], IWMCodecLeakyBucket interface [Media Foundation],described, codecapi.iwmcodecleakybucketinterface, mf.iwmcodecleakybucketinterface, wmcodecdsp/IWMCodecLeakyBucket
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
 - IWMCodecLeakyBucket
 - wmcodecdsp/IWMCodecLeakyBucket
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
 - IWMCodecLeakyBucket
---

# IWMCodecLeakyBucket interface


## -description

Configures the "leaky bucket" parameters on a video encoder.

This interface is implemented by all of the encoder objects. You can get a pointer to the <b>IWMCodecLeakyBucket</b> interface for a Windows Media video encoder by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of any other interface on the object, such as <a href="/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>. This interface is not  implemented on any of the decoders.

## -inheritance

The <b>IWMCodecLeakyBucket</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecLeakyBucket</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/the-leaky-bucket-buffer-model">The Leaky Bucket Buffer Model</a>
