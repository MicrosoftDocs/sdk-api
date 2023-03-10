---
UID: NN:vmr9.IVMRImagePresenter9
title: IVMRImagePresenter9 (vmr9.h)
description: The IVMRImagePresenter9 interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRImagePresenter9","IVMRImagePresenter9 interface [DirectShow]","IVMRImagePresenter9 interface [DirectShow]","described","IVMRImagePresenter9Interface","dshow.ivmrimagepresenter9","vmr9/IVMRImagePresenter9"]
old-location: dshow\ivmrimagepresenter9.htm
tech.root: dshow
ms.assetid: 2c18cdd6-af97-4db2-80b5-bab4cfa25f7d
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenter9, IVMRImagePresenter9 interface [DirectShow], IVMRImagePresenter9 interface [DirectShow],described, IVMRImagePresenter9Interface, dshow.ivmrimagepresenter9, vmr9/IVMRImagePresenter9
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
 - IVMRImagePresenter9
 - vmr9/IVMRImagePresenter9
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
 - IVMRImagePresenter9
---

# IVMRImagePresenter9 interface


## -description

The <code>IVMRImagePresenter9</code> interface is implemented by the default allocator-presenter for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in allocator-presenter that an application provides for the VMR-9. The VMR-9 uses this interface to inform the allocator-presenter that it should present the video frame contained in the supplied Direct3D surface. Applications do not use this interface.

## -inheritance

The <b>IVMRImagePresenter9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRImagePresenter9</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
