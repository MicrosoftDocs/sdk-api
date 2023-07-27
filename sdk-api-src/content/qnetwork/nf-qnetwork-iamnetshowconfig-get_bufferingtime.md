---
UID: NF:qnetwork.IAMNetShowConfig.get_BufferingTime
title: IAMNetShowConfig::get_BufferingTime (qnetwork.h)
description: The get_BufferingTime method retrieves the buffering time.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_BufferingTime method","IAMNetShowConfig.get_BufferingTime","IAMNetShowConfig::get_BufferingTime","IAMNetShowConfigget_BufferingTime","dshow.iamnetshowconfig_get_bufferingtime","get_BufferingTime","get_BufferingTime method [DirectShow]","get_BufferingTime method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_BufferingTime"]
old-location: dshow\iamnetshowconfig_get_bufferingtime.htm
tech.root: dshow
ms.assetid: 8594f8dd-9545-4e6d-b1d7-9a278dcb4129
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],get_BufferingTime method, IAMNetShowConfig.get_BufferingTime, IAMNetShowConfig::get_BufferingTime, IAMNetShowConfigget_BufferingTime, dshow.iamnetshowconfig_get_bufferingtime, get_BufferingTime, get_BufferingTime method [DirectShow], get_BufferingTime method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_BufferingTime
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
 - IAMNetShowConfig::get_BufferingTime
 - qnetwork/IAMNetShowConfig::get_BufferingTime
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
 - IAMNetShowConfig.get_BufferingTime
---

# IAMNetShowConfig::get_BufferingTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_BufferingTime</code> method retrieves the buffering time.

## -parameters

### -param pBufferingTime

Pointer that receives the buffering time, in seconds.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>