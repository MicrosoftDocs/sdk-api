---
UID: NF:qnetwork.IAMNetShowConfig.get_EnableMulticast
title: IAMNetShowConfig::get_EnableMulticast (qnetwork.h)
description: The get_EnableMulticast method queries whether multicast-type streaming is enabled.
helpviewer_keywords: ["IAMNetShowConfig interface [DirectShow]","get_EnableMulticast method","IAMNetShowConfig.get_EnableMulticast","IAMNetShowConfig::get_EnableMulticast","IAMNetShowConfigget_EnableMulticast","dshow.iamnetshowconfig_get_enablemulticast","get_EnableMulticast","get_EnableMulticast method [DirectShow]","get_EnableMulticast method [DirectShow]","IAMNetShowConfig interface","qnetwork/IAMNetShowConfig::get_EnableMulticast"]
old-location: dshow\iamnetshowconfig_get_enablemulticast.htm
tech.root: dshow
ms.assetid: dae5c0ad-a41e-424c-a04d-69dbe7264143
ms.date: 4/26/2023
ms.keywords: IAMNetShowConfig interface [DirectShow],get_EnableMulticast method, IAMNetShowConfig.get_EnableMulticast, IAMNetShowConfig::get_EnableMulticast, IAMNetShowConfigget_EnableMulticast, dshow.iamnetshowconfig_get_enablemulticast, get_EnableMulticast, get_EnableMulticast method [DirectShow], get_EnableMulticast method [DirectShow],IAMNetShowConfig interface, qnetwork/IAMNetShowConfig::get_EnableMulticast
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
 - IAMNetShowConfig::get_EnableMulticast
 - qnetwork/IAMNetShowConfig::get_EnableMulticast
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
 - IAMNetShowConfig.get_EnableMulticast
---

# IAMNetShowConfig::get_EnableMulticast


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_EnableMulticast</code> method queries whether multicast-type streaming is enabled.

## -parameters

### -param pEnableMulticast

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowconfig">IAMNetShowConfig Interface</a>