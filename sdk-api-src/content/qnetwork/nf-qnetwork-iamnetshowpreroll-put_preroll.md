---
UID: NF:qnetwork.IAMNetShowPreroll.put_Preroll
title: IAMNetShowPreroll::put_Preroll (qnetwork.h)
description: The put_Preroll method specifies whether the filter should start prerolling.
helpviewer_keywords: ["IAMNetShowPreroll interface [DirectShow]","put_Preroll method","IAMNetShowPreroll.put_Preroll","IAMNetShowPreroll::put_Preroll","IAMNetShowPrerollput_Preroll","dshow.iamnetshowpreroll_put_preroll","put_Preroll","put_Preroll method [DirectShow]","put_Preroll method [DirectShow]","IAMNetShowPreroll interface","qnetwork/IAMNetShowPreroll::put_Preroll"]
old-location: dshow\iamnetshowpreroll_put_preroll.htm
tech.root: dshow
ms.assetid: 3296f0ab-2be8-4693-99bd-5dae0672df26
ms.date: 4/26/2023
ms.keywords: IAMNetShowPreroll interface [DirectShow],put_Preroll method, IAMNetShowPreroll.put_Preroll, IAMNetShowPreroll::put_Preroll, IAMNetShowPrerollput_Preroll, dshow.iamnetshowpreroll_put_preroll, put_Preroll, put_Preroll method [DirectShow], put_Preroll method [DirectShow],IAMNetShowPreroll interface, qnetwork/IAMNetShowPreroll::put_Preroll
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowPreroll::put_Preroll
 - qnetwork/IAMNetShowPreroll::put_Preroll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowPreroll.put_Preroll
---

# IAMNetShowPreroll::put_Preroll


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Preroll</code> method specifies whether the filter should start prerolling.

## -parameters

### -param fPreroll

Specifies one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Begin prerolling.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Stop prerolling.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowpreroll">IAMNetShowPreroll Interface</a>