---
UID: NF:strmif.IVMRImagePresenterConfig.GetRenderingPrefs
title: IVMRImagePresenterConfig::GetRenderingPrefs (strmif.h)
description: The GetRenderingPrefs method retrieves the current rendering preferences from the VMR-7 filter's allocator-presenter.
helpviewer_keywords: ["GetRenderingPrefs","GetRenderingPrefs method [DirectShow]","GetRenderingPrefs method [DirectShow]","IVMRImagePresenterConfig interface","IVMRImagePresenterConfig interface [DirectShow]","GetRenderingPrefs method","IVMRImagePresenterConfig.GetRenderingPrefs","IVMRImagePresenterConfig::GetRenderingPrefs","IVMRImagePresenterConfigGetRenderingPrefs","dshow.ivmrimagepresenterconfig_getrenderingprefs","strmif/IVMRImagePresenterConfig::GetRenderingPrefs"]
old-location: dshow\ivmrimagepresenterconfig_getrenderingprefs.htm
tech.root: dshow
ms.assetid: e9ca9c02-e38d-4600-aee8-08afd03423ad
ms.date: 4/26/2023
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig interface, IVMRImagePresenterConfig interface [DirectShow],GetRenderingPrefs method, IVMRImagePresenterConfig.GetRenderingPrefs, IVMRImagePresenterConfig::GetRenderingPrefs, IVMRImagePresenterConfigGetRenderingPrefs, dshow.ivmrimagepresenterconfig_getrenderingprefs, strmif/IVMRImagePresenterConfig::GetRenderingPrefs
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
 - IVMRImagePresenterConfig::GetRenderingPrefs
 - strmif/IVMRImagePresenterConfig::GetRenderingPrefs
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
 - IVMRImagePresenterConfig.GetRenderingPrefs
---

# IVMRImagePresenterConfig::GetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRenderingPrefs</code> method retrieves the current rendering preferences from the VMR-7 filter's allocator-presenter.



The VMR-7 filter's <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingprefs">IVMRFilterConfig::GetRenderingPrefs</a> method calls through to this method.

## -parameters

### -param dwRenderFlags [out]

Receives a bitwise OR of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-vmrrenderprefs">VMRRenderPrefs</a> enumeration, indicating the current rendering settings on the allocator-presenter.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>