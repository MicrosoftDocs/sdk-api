---
UID: NN:vmr9.IVMRVideoStreamControl9
title: IVMRVideoStreamControl9 (vmr9.h)
description: The IVMRVideoStreamControl9 interface is implemented on each input pin of the Video Mixing Renderer Filter 9.
helpviewer_keywords: ["IVMRVideoStreamControl9","IVMRVideoStreamControl9 interface [DirectShow]","IVMRVideoStreamControl9 interface [DirectShow]","described","IVMRVideoStreamControl9Interface","dshow.ivmrvideostreamcontrol9","vmr9/IVMRVideoStreamControl9"]
old-location: dshow\ivmrvideostreamcontrol9.htm
tech.root: dshow
ms.assetid: df642ebb-058b-41db-95d3-d7d3bf9a6dd0
ms.date: 12/05/2018
ms.keywords: IVMRVideoStreamControl9, IVMRVideoStreamControl9 interface [DirectShow], IVMRVideoStreamControl9 interface [DirectShow],described, IVMRVideoStreamControl9Interface, dshow.ivmrvideostreamcontrol9, vmr9/IVMRVideoStreamControl9
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRVideoStreamControl9
 - vmr9/IVMRVideoStreamControl9
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
 - IVMRVideoStreamControl9
---

# IVMRVideoStreamControl9 interface


## -description

The <code>IVMRVideoStreamControl9</code> interface is implemented on each input pin of the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>. The interface operates on the input stream represented by the pin. This interface is used by upstream filters (typically decoders) to get or set the active state of individual streams. Applications in general should not use this interface.

## -inheritance

The <b>IVMRVideoStreamControl9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRVideoStreamControl9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
