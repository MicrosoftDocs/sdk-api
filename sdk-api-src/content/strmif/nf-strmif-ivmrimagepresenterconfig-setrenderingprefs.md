---
UID: NF:strmif.IVMRImagePresenterConfig.SetRenderingPrefs
title: IVMRImagePresenterConfig::SetRenderingPrefs (strmif.h)
description: The SetRenderingPrefs method sets the rendering preferences on the VMR-7 filter's allocator-presenter.
helpviewer_keywords: ["IVMRImagePresenterConfig interface [DirectShow]","SetRenderingPrefs method","IVMRImagePresenterConfig.SetRenderingPrefs","IVMRImagePresenterConfig::SetRenderingPrefs","IVMRImagePresenterConfigSetRenderingPrefs","SetRenderingPrefs","SetRenderingPrefs method [DirectShow]","SetRenderingPrefs method [DirectShow]","IVMRImagePresenterConfig interface","dshow.ivmrimagepresenterconfig_setrenderingprefs","strmif/IVMRImagePresenterConfig::SetRenderingPrefs"]
old-location: dshow\ivmrimagepresenterconfig_setrenderingprefs.htm
tech.root: dshow
ms.assetid: 22bb6d52-2201-429d-bd1a-d031c9b017ae
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenterConfig interface [DirectShow],SetRenderingPrefs method, IVMRImagePresenterConfig.SetRenderingPrefs, IVMRImagePresenterConfig::SetRenderingPrefs, IVMRImagePresenterConfigSetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig interface, dshow.ivmrimagepresenterconfig_setrenderingprefs, strmif/IVMRImagePresenterConfig::SetRenderingPrefs
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
 - IVMRImagePresenterConfig::SetRenderingPrefs
 - strmif/IVMRImagePresenterConfig::SetRenderingPrefs
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
 - IVMRImagePresenterConfig.SetRenderingPrefs
---

# IVMRImagePresenterConfig::SetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRenderingPrefs</code> method sets the rendering preferences on the VMR-7 filter's allocator-presenter.



The VMR-7 filter's <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs">IVMRFilterConfig::SetRenderingPrefs</a> method calls through to this method.

## -parameters

### -param dwRenderFlags [in]

A bitwise OR combination of <a href="/windows/desktop/api/strmif/ne-strmif-vmrrenderprefs">VMRRenderPrefs</a> flags that will be used to configure the allocator-presenter.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>