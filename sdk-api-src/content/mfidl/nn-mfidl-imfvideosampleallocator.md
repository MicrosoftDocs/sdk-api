---
UID: NN:mfidl.IMFVideoSampleAllocator
title: IMFVideoSampleAllocator (mfidl.h)
description: Allocates video samples for a video media sink.
helpviewer_keywords: ["IMFVideoSampleAllocator","IMFVideoSampleAllocator interface [Media Foundation]","IMFVideoSampleAllocator interface [Media Foundation]","described","bef92133-ae6c-4013-9210-5e0f0be2002c","mf.imfvideosampleallocator","mfidl/IMFVideoSampleAllocator"]
old-location: mf\imfvideosampleallocator.htm
tech.root: mf
ms.assetid: bef92133-ae6c-4013-9210-5e0f0be2002c
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocator, IMFVideoSampleAllocator interface [Media Foundation], IMFVideoSampleAllocator interface [Media Foundation],described, bef92133-ae6c-4013-9210-5e0f0be2002c, mf.imfvideosampleallocator, mfidl/IMFVideoSampleAllocator
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoSampleAllocator
 - mfidl/IMFVideoSampleAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoSampleAllocator
---

# IMFVideoSampleAllocator interface


## -description

Allocates video samples for a video media sink.

The stream sinks on the enhanced video renderer (EVR) expose this interface as a service. To obtain a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> using the service identifier MR_VIDEO_ACCELERATION_SERVICE. Custom media sinks can also implement this interface. The Media Session uses this interface to allocate samples for the EVR, unless the upstream decoder supports DirectX Video Acceleration (DXVA).

## -inheritance

The <b>IMFVideoSampleAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoSampleAllocator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
