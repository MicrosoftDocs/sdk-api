---
UID: NF:strmif.IVMRImagePresenter.StopPresenting
title: IVMRImagePresenter::StopPresenting (strmif.h)
description: The StopPresenting method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.
helpviewer_keywords: ["IVMRImagePresenter interface [DirectShow]","StopPresenting method","IVMRImagePresenter.StopPresenting","IVMRImagePresenter::StopPresenting","IVMRImagePresenterStopPresenting","StopPresenting","StopPresenting method [DirectShow]","StopPresenting method [DirectShow]","IVMRImagePresenter interface","dshow.ivmrimagepresenter_stoppresenting","strmif/IVMRImagePresenter::StopPresenting"]
old-location: dshow\ivmrimagepresenter_stoppresenting.htm
tech.root: dshow
ms.assetid: b6887c66-56ba-4ee6-a740-73213ac088d5
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenter interface [DirectShow],StopPresenting method, IVMRImagePresenter.StopPresenting, IVMRImagePresenter::StopPresenting, IVMRImagePresenterStopPresenting, StopPresenting, StopPresenting method [DirectShow], StopPresenting method [DirectShow],IVMRImagePresenter interface, dshow.ivmrimagepresenter_stoppresenting, strmif/IVMRImagePresenter::StopPresenting
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
 - IVMRImagePresenter::StopPresenting
 - strmif/IVMRImagePresenter::StopPresenting
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
 - IVMRImagePresenter.StopPresenting
---

# IVMRImagePresenter::StopPresenting


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>StopPresenting</code> method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.

## -parameters

### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<code>StopPresenting</code> can be called only when the VMR is in a running state.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenter">IVMRImagePresenter Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenter-startpresenting">IVMRImagePresenter::StartPresenting</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>