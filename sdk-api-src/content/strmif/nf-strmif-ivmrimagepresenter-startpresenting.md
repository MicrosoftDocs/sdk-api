---
UID: NF:strmif.IVMRImagePresenter.StartPresenting
title: IVMRImagePresenter::StartPresenting (strmif.h)
description: The StartPresenting method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.
helpviewer_keywords: ["IVMRImagePresenter interface [DirectShow]","StartPresenting method","IVMRImagePresenter.StartPresenting","IVMRImagePresenter::StartPresenting","IVMRImagePresenterStartPresenting","StartPresenting","StartPresenting method [DirectShow]","StartPresenting method [DirectShow]","IVMRImagePresenter interface","dshow.ivmrimagepresenter_startpresenting","strmif/IVMRImagePresenter::StartPresenting"]
old-location: dshow\ivmrimagepresenter_startpresenting.htm
tech.root: dshow
ms.assetid: b97debae-d792-4c9b-a171-11ef2a73e987
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenter interface [DirectShow],StartPresenting method, IVMRImagePresenter.StartPresenting, IVMRImagePresenter::StartPresenting, IVMRImagePresenterStartPresenting, StartPresenting, StartPresenting method [DirectShow], StartPresenting method [DirectShow],IVMRImagePresenter interface, dshow.ivmrimagepresenter_startpresenting, strmif/IVMRImagePresenter::StartPresenting
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
 - IVMRImagePresenter::StartPresenting
 - strmif/IVMRImagePresenter::StartPresenting
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
 - IVMRImagePresenter.StartPresenting
---

# IVMRImagePresenter::StartPresenting


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StartPresenting</code> method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.

## -parameters

### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<b>PresentImage</b> can be called when the filter is in either a running or a paused state. <code>StartPresenting</code> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <b>PresentImage</b> will be called before <code>StartPresenting</code>.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenter">IVMRImagePresenter Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenter-stoppresenting">IVMRImagePresenter::StopPresenting</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>