---
UID: NN:strmif.IVMRImagePresenterExclModeConfig
title: IVMRImagePresenterExclModeConfig (strmif.h)
description: The IVMRImagePresenterExclModeConfig interface inherits from IVMRImagePresenterConfig and provides methods for setting and retrieving the rendering preferences on the Exclusive Mode Allocator-Presenter.
helpviewer_keywords: ["IVMRImagePresenterExclModeConfig","IVMRImagePresenterExclModeConfig interface [DirectShow]","IVMRImagePresenterExclModeConfig interface [DirectShow]","described","dshow.ivmrimagepresenterexclmodeconfig","strmif/IVMRImagePresenterExclModeConfig"]
old-location: dshow\ivmrimagepresenterexclmodeconfig.htm
tech.root: dshow
ms.assetid: 67c9675c-c0fd-44f6-bdeb-ac3f73e937cc
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenterExclModeConfig, IVMRImagePresenterExclModeConfig interface [DirectShow], IVMRImagePresenterExclModeConfig interface [DirectShow],described, dshow.ivmrimagepresenterexclmodeconfig, strmif/IVMRImagePresenterExclModeConfig
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
 - IVMRImagePresenterExclModeConfig
 - strmif/IVMRImagePresenterExclModeConfig
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
 - IVMRImagePresenterExclModeConfig
---

# IVMRImagePresenterExclModeConfig interface


## -description

The <code>IVMRImagePresenterExclModeConfig</code> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a> and provides methods for setting and retrieving the rendering preferences on the Exclusive Mode Allocator-Presenter. This interface is exposed on the DirectDraw Exclusive Mode Allocator-Presenter object. When applications run in DirectDraw Exclusive Mode, they must create their own DirectDraw object, configure the VMR to use the Exclusive Mode Allocator-Presenter, and use this interface to inform the VMR about the DirectDraw object and the primary surface associated with it. For more information, see <a href="/windows/desktop/DirectShow/directdraw-exclusive-mode">DirectDraw Exclusive Mode</a>.

## -inheritance

The <b>IVMRImagePresenterExclModeConfig</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a>. <b>IVMRImagePresenterExclModeConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
