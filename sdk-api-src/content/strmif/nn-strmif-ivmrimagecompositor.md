---
UID: NN:strmif.IVMRImageCompositor
title: IVMRImageCompositor (strmif.h)
description: The IVMRImageCompositor interface is implemented by the default compositor for the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRImageCompositor","IVMRImageCompositor interface [DirectShow]","IVMRImageCompositor interface [DirectShow]","described","IVMRImageCompositorInterface","dshow.ivmrimagecompositor","strmif/IVMRImageCompositor"]
old-location: dshow\ivmrimagecompositor.htm
tech.root: dshow
ms.assetid: d905e871-c156-4140-bb3f-a19fa0cd79be
ms.date: 12/05/2018
ms.keywords: IVMRImageCompositor, IVMRImageCompositor interface [DirectShow], IVMRImageCompositor interface [DirectShow],described, IVMRImageCompositorInterface, dshow.ivmrimagecompositor, strmif/IVMRImageCompositor
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRImageCompositor
 - strmif/IVMRImageCompositor
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
 - IVMRImageCompositor
---

# IVMRImageCompositor interface


## -description

The <code>IVMRImageCompositor</code> interface is implemented by the default compositor for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in compositor that an application provides for the VMR-7. The VMR-7 calls the methods on this interface to inform the Compositor that it should composite the incoming video frames into a single output frame. Applications do not use this interface.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrimagecompositor9">IVMRImageCompositor9</a> interface.

## -inheritance

The <b>IVMRImageCompositor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImageCompositor</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
