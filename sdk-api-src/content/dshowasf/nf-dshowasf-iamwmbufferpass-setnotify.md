---
UID: NF:dshowasf.IAMWMBufferPass.SetNotify
title: IAMWMBufferPass::SetNotify (dshowasf.h)
description: The SetNotify method is used by applications to provide the WM ASF Writer or WM ASF Reader filter with a pointer to the application's IAMWMBufferPassCallback interface.
helpviewer_keywords: ["IAMWMBufferPass interface [windows Media Format]","SetNotify method","IAMWMBufferPass.SetNotify","IAMWMBufferPass::SetNotify","IAMWMBufferPassSetNotify","SetNotify","SetNotify method [windows Media Format]","SetNotify method [windows Media Format]","IAMWMBufferPass interface","dshowasf/IAMWMBufferPass::SetNotify","wmformat.iamwmbufferpass_setnotify"]
old-location: wmformat\iamwmbufferpass_setnotify.htm
tech.root: wmformat
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
ms.date: 4/26/2023
ms.keywords: IAMWMBufferPass interface [windows Media Format],SetNotify method, IAMWMBufferPass.SetNotify, IAMWMBufferPass::SetNotify, IAMWMBufferPassSetNotify, SetNotify, SetNotify method [windows Media Format], SetNotify method [windows Media Format],IAMWMBufferPass interface, dshowasf/IAMWMBufferPass::SetNotify, wmformat.iamwmbufferpass_setnotify
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMWMBufferPass::SetNotify
 - dshowasf/IAMWMBufferPass::SetNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dshowasf.h
api_name:
 - IAMWMBufferPass.SetNotify
---

# IAMWMBufferPass::SetNotify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetNotify</b> method is used by applications to provide the WM ASF Writer or <a href="/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> filter with a pointer to the application's <a href="/previous-versions/windows/desktop/legacy/dd798277(v=vs.85)">IAMWMBufferPassCallback</a> interface.

## -parameters

### -param pCallback [in]

Pointer to the application's <b>IAMWMBufferPassCallback</b> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method before putting the filter graph into the run state.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd798276(v=vs.85)">IAMWMBufferPass Interface</a>