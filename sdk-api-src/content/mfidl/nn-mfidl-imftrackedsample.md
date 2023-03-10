---
UID: NN:mfidl.IMFTrackedSample
title: IMFTrackedSample (mfidl.h)
description: Tracks the reference counts on a video media sample.
helpviewer_keywords: ["4ad4b14c-94af-4314-8a16-163579dec67f","IMFTrackedSample","IMFTrackedSample interface [Media Foundation]","IMFTrackedSample interface [Media Foundation]","described","mf.imftrackedsample","mfidl/IMFTrackedSample"]
old-location: mf\imftrackedsample.htm
tech.root: mf
ms.assetid: 4ad4b14c-94af-4314-8a16-163579dec67f
ms.date: 12/05/2018
ms.keywords: 4ad4b14c-94af-4314-8a16-163579dec67f, IMFTrackedSample, IMFTrackedSample interface [Media Foundation], IMFTrackedSample interface [Media Foundation],described, mf.imftrackedsample, mfidl/IMFTrackedSample
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFTrackedSample
 - mfidl/IMFTrackedSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTrackedSample
---

# IMFTrackedSample interface


## -description

Tracks the reference counts on a video media sample. Video samples created by the <a href="/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface">MFCreateVideoSampleFromSurface</a> function expose this interface.

## -inheritance

The <b>IMFTrackedSample</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTrackedSample</b> also has these types of members:

## -remarks

Use this interface to determine whether it is safe to delete or re-use the buffer contained in a sample. One object assigns itself as the owner of the video sample by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imftrackedsample-setallocator">SetAllocator</a>. When all objects release their reference counts on the sample, the owner's callback method is invoked.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
