---
UID: NF:strmif.IVMRImagePresenter.PresentImage
title: IVMRImagePresenter::PresentImage (strmif.h)
description: The PresentImage method is called at precisely the moment this video frame should be presented.
helpviewer_keywords: ["IVMRImagePresenter interface [DirectShow]","PresentImage method","IVMRImagePresenter.PresentImage","IVMRImagePresenter::PresentImage","IVMRImagePresenterPresentImage","PresentImage","PresentImage method [DirectShow]","PresentImage method [DirectShow]","IVMRImagePresenter interface","dshow.ivmrimagepresenter_presentimage","strmif/IVMRImagePresenter::PresentImage"]
old-location: dshow\ivmrimagepresenter_presentimage.htm
tech.root: dshow
ms.assetid: df6bf45d-df92-4655-862c-704a12a62ff9
ms.date: 12/05/2018
ms.keywords: IVMRImagePresenter interface [DirectShow],PresentImage method, IVMRImagePresenter.PresentImage, IVMRImagePresenter::PresentImage, IVMRImagePresenterPresentImage, PresentImage, PresentImage method [DirectShow], PresentImage method [DirectShow],IVMRImagePresenter interface, dshow.ivmrimagepresenter_presentimage, strmif/IVMRImagePresenter::PresentImage
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
 - IVMRImagePresenter::PresentImage
 - strmif/IVMRImagePresenter::PresentImage
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
 - IVMRImagePresenter.PresentImage
---

# IVMRImagePresenter::PresentImage


## -description

The <code>PresentImage</code> method is called at precisely the moment this video frame should be presented.

## -parameters

### -param dwUserID [in]

An application-defined DWORD_PTR that uniquely identifies this instance of the VMR in scenarios when multiple instances of the VMR are being used with a single instance of an Allocator-Presenter. See Remarks

### -param lpPresInfo [in]

Specifies the [VMRPRESENTATIONINFO](/windows/desktop/api/strmif/ns-strmif-vmrpresentationinfo) structure.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<code>PresentImage</code> can be called when the filter is in either a running or a paused state. <b>StartPresenting</b> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <code>PresentImage</code> will be called before <b>StartPresenting</b>.

Applications can create custom blending effects by using a single instance of an Allocator-Presenter with multiple instances of the VMR either in a single filter graph or in multiple filter graphs. Using the allocator presenter in this way enables applications to blend streams from different filter graphs, or blend different streams within the same filter graph. If you are using a single instance of the VMR, set this value to zero.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenter">IVMRImagePresenter Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>