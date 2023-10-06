---
UID: NF:qnetwork.IAMNetShowConfig.put_BufferingTime
title: IAMNetShowConfig::put_BufferingTime (qnetwork.h)
description: The put_BufferingTime method specifies the buffering time.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","put_BufferingTime method","IAMNetShowConfig.put_BufferingTime","IAMNetShowConfig::put_BufferingTime","IAMNetShowConfigput_BufferingTime","dshow.iamnetshowconfig_put_bufferingtime","put_BufferingTime","put_BufferingTime method [DirectShow]","put_BufferingTime method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::put_BufferingTime"]
old-location: dshow\iamnetshowconfig_put_bufferingtime.htm
tech.root: dshow
ms.assetid: 60dea6f3-b45f-44a1-ba21-eb71206b2fb5
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],put_BufferingTime method, IAMNetShowConfig.put_BufferingTime, IAMNetShowConfig::put_BufferingTime, IAMNetShowConfigput_BufferingTime, dshow.iamnetshowconfig_put_bufferingtime, put_BufferingTime, put_BufferingTime method [DirectShow], put_BufferingTime method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::put_BufferingTime
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
 - IAMNetShowConfig::put_BufferingTime
 - qnetwork/IAMNetShowConfig::put_BufferingTime
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
 - IAMNetShowConfig.put_BufferingTime
---

# IAMNetShowConfig::put_BufferingTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_BufferingTime</code> method specifies the buffering time.

## -parameters

### -param BufferingTime

Specifies the buffering time, in seconds.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>