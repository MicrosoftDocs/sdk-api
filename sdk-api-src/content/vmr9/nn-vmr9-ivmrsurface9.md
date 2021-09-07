---
UID: NN:vmr9.IVMRSurface9
title: IVMRSurface9 (vmr9.h)
description: The IVMRSurface9 interface is implemented on the media samples used by the Video Mixing Renderer Filter 9.
helpviewer_keywords: ["IVMRSurface9","IVMRSurface9 interface [DirectShow]","IVMRSurface9 interface [DirectShow]","described","IVMRSurface9Interface","dshow.ivmrsurface9","vmr9/IVMRSurface9"]
old-location: dshow\ivmrsurface9.htm
tech.root: dshow
ms.assetid: b24dae7d-5e88-4973-8507-8bd13cdccbde
ms.date: 12/05/2018
ms.keywords: IVMRSurface9, IVMRSurface9 interface [DirectShow], IVMRSurface9 interface [DirectShow],described, IVMRSurface9Interface, dshow.ivmrsurface9, vmr9/IVMRSurface9
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
 - IVMRSurface9
 - vmr9/IVMRSurface9
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
 - IVMRSurface9
---

# IVMRSurface9 interface


## -description

The <code>IVMRSurface9</code> interface is implemented on the media samples used by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>. Filters can use this interface to access the underlying Direct3D surface on which the media sample is based. Filters must always lock and unlock the surface using the methods available on this interface. Filters must never call lock or unlock directly on the Direct3D surface interface returned from the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurface-getsurface">GetSurface</a> method. Applications do not use this interface.

## -inheritance

The <b>IVMRSurface9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurface9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
