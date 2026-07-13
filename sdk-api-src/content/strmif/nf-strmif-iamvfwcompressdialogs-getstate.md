---
UID: NF:strmif.IAMVfwCompressDialogs.GetState
title: IAMVfwCompressDialogs::GetState (strmif.h)
description: The GetState method retrieves the current configuration settings for the VCM codec currently being used.
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IAMVfwCompressDialogs interface","IAMVfwCompressDialogs interface [DirectShow]","GetState method","IAMVfwCompressDialogs.GetState","IAMVfwCompressDialogs::GetState","IAMVfwCompressDialogsGetState","dshow.iamvfwcompressdialogs_getstate","strmif/IAMVfwCompressDialogs::GetState"]
old-location: dshow\iamvfwcompressdialogs_getstate.htm
tech.root: dshow
ms.assetid: a010fd8a-ad4a-4b52-abfe-a2db8cd15b65
ms.date: 4/26/2023
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IAMVfwCompressDialogs interface, IAMVfwCompressDialogs interface [DirectShow],GetState method, IAMVfwCompressDialogs.GetState, IAMVfwCompressDialogs::GetState, IAMVfwCompressDialogsGetState, dshow.iamvfwcompressdialogs_getstate, strmif/IAMVfwCompressDialogs::GetState
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMVfwCompressDialogs::GetState
 - strmif/IAMVfwCompressDialogs::GetState
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
 - IAMVfwCompressDialogs.GetState
---

# IAMVfwCompressDialogs::GetState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetState</code> method retrieves the current configuration settings for the VCM codec currently being used.

## -parameters

### -param pState [out]

State of the VCM codec.

### -param pcbState [in, out]

Pointer to the size of the state.

## -returns

Return value varies depending on the implementation within each driver.

## -remarks

This method calls the  <a href="/windows/desktop/api/vfw/nf-vfw-icgetstate">ICGetState</a> macro.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcompressdialogs">IAMVfwCompressDialogs Interface</a>