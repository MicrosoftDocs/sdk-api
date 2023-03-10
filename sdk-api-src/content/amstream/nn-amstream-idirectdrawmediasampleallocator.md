---
UID: NN:amstream.IDirectDrawMediaSampleAllocator
title: IDirectDrawMediaSampleAllocator (amstream.h)
description: The IDirectDrawMediaSampleAllocator interface allocates samples that contain DirectDraw surfaces.The Overlay Mixer filter's input pin creates an allocator that implements this interface.
helpviewer_keywords: ["IDirectDrawMediaSampleAllocator","IDirectDrawMediaSampleAllocator interface [DirectShow]","IDirectDrawMediaSampleAllocator interface [DirectShow]","described","IDirectDrawMediaSampleAllocatorInterface","amstream/IDirectDrawMediaSampleAllocator","dshow.idirectdrawmediasampleallocator"]
old-location: dshow\idirectdrawmediasampleallocator.htm
tech.root: dshow
ms.assetid: 35fd81ce-058a-4caf-b1de-f669be586f33
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaSampleAllocator, IDirectDrawMediaSampleAllocator interface [DirectShow], IDirectDrawMediaSampleAllocator interface [DirectShow],described, IDirectDrawMediaSampleAllocatorInterface, amstream/IDirectDrawMediaSampleAllocator, dshow.idirectdrawmediasampleallocator
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IDirectDrawMediaSampleAllocator
 - amstream/IDirectDrawMediaSampleAllocator
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
 - IDirectDrawMediaSampleAllocator
---

# IDirectDrawMediaSampleAllocator interface


## -description

The <code>IDirectDrawMediaSampleAllocator</code> interface allocates samples that contain DirectDraw surfaces.

The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter's input pin creates an allocator that implements this interface. This allocator allocates <a href="/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample">IDirectDrawMediaSample</a> media samples that also support the <a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface.

Decoder filters should not have to use this interface to connect to the Overlay Mixer. Applications never use this interface.

## -inheritance

The <b>IDirectDrawMediaSampleAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawMediaSampleAllocator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

