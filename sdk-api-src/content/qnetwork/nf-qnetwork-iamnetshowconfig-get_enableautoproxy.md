---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableAutoProxy
title: IAMNetShowConfig::get_EnableAutoProxy (qnetwork.h)
description: The get_EnableAutoProxy method queries whether the control or filter should use the browser's proxy settings.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_EnableAutoProxy method","IAMNetShowConfig.get_EnableAutoProxy","IAMNetShowConfig::get_EnableAutoProxy","IAMNetShowConfigget_EnableAutoProxy","dshow.iamnetshowconfig_get_enableautoproxy","get_EnableAutoProxy","get_EnableAutoProxy method [DirectShow]","get_EnableAutoProxy method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_EnableAutoProxy"]
old-location: dshow\iamnetshowconfig_get_enableautoproxy.htm
tech.root: dshow
ms.assetid: 7037f326-3320-4e4a-8f6f-feda1a306c2d
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableAutoProxy method, IAMNetShowConfig.get_EnableAutoProxy, IAMNetShowConfig::get_EnableAutoProxy, IAMNetShowConfigget_EnableAutoProxy, dshow.iamnetshowconfig_get_enableautoproxy, get_EnableAutoProxy, get_EnableAutoProxy method [DirectShow], get_EnableAutoProxy method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableAutoProxy
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
 - IAMNetShowConfig::get_EnableAutoProxy
 - qnetwork/IAMNetShowConfig::get_EnableAutoProxy
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
 - IAMNetShowConfig.get_EnableAutoProxy
---

# IAMNetShowConfig::get_EnableAutoProxy


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_EnableAutoProxy</code> method queries whether the control or filter should use the browser's proxy settings.

## -parameters

### -param pEnableAutoProxy

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This flag is <b>TRUE</b> by default.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>