---
UID: NN:vmr9.IVMRImagePresenterConfig9
title: IVMRImagePresenterConfig9 (vmr9.h)
description: The IVMRImagePresenterConfig interface provides methods for setting the rendering preferences on the allocator-presenter used by the Video Mixing Renderer Filter 9 (VMR-9).Applications should not use this interface directly.
helpviewer_keywords: ["IVMRImagePresenterConfig9","IVMRImagePresenterConfig9 interface [DirectShow]","IVMRImagePresenterConfig9 interface [DirectShow]","described","IVMRImagePresenterConfig9Interface","dshow.ivmrimagepresenterconfig9","vmr9/IVMRImagePresenterConfig9"]
old-location: dshow\ivmrimagepresenterconfig9.htm
tech.root: dshow
ms.assetid: fc3c9b4d-0213-47d5-96e4-db582c80ca4e
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenterConfig9, IVMRImagePresenterConfig9 interface [DirectShow], IVMRImagePresenterConfig9 interface [DirectShow],described, IVMRImagePresenterConfig9Interface, dshow.ivmrimagepresenterconfig9, vmr9/IVMRImagePresenterConfig9
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
 - IVMRImagePresenterConfig9
 - vmr9/IVMRImagePresenterConfig9
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
 - IVMRImagePresenterConfig9
---

# IVMRImagePresenterConfig9 interface


## -description

The <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a> interface provides methods for setting the rendering preferences on the allocator-presenter used by the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9).

Applications should not use this interface directly. The VMR-9 filter's <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9</a> interface calls methods on this interface. The default allocator-presenter implements this interface. Custom allocator-presenters can also expose this interface.

## -inheritance

The <b>IVMRImagePresenterConfig9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImagePresenterConfig9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
