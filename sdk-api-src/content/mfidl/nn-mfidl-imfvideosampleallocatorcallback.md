---
UID: NN:mfidl.IMFVideoSampleAllocatorCallback
title: IMFVideoSampleAllocatorCallback (mfidl.h)
description: Enables an application to track video samples allocated by the enhanced video renderer (EVR).
helpviewer_keywords: ["IMFVideoSampleAllocatorCallback","IMFVideoSampleAllocatorCallback interface [Media Foundation]","IMFVideoSampleAllocatorCallback interface [Media Foundation]","described","mf.imfvideosampleallocatorcallback","mfidl/IMFVideoSampleAllocatorCallback"]
old-location: mf\imfvideosampleallocatorcallback.htm
tech.root: mf
ms.assetid: 7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac
ms.date: 12/05/2018
ms.keywords: IMFVideoSampleAllocatorCallback, IMFVideoSampleAllocatorCallback interface [Media Foundation], IMFVideoSampleAllocatorCallback interface [Media Foundation],described, mf.imfvideosampleallocatorcallback, mfidl/IMFVideoSampleAllocatorCallback
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFVideoSampleAllocatorCallback
 - mfidl/IMFVideoSampleAllocatorCallback
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
 - IMFVideoSampleAllocatorCallback
---

# IMFVideoSampleAllocatorCallback interface


## -description

Enables an application to track video samples allocated by the enhanced video renderer (EVR).

The stream sinks on the EVR expose this interface as a service. To get a pointer to the interface, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method, using the <b>MR_VIDEO_ACCELERATION_SERVICE</b> service identifier.

## -inheritance

The <b>IMFVideoSampleAllocatorCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoSampleAllocatorCallback</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator">IMFVideoSampleAllocator</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
