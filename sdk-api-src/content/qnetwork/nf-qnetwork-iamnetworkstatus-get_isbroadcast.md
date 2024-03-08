---
UID: NF:qnetwork.IAMNetworkStatus.get_IsBroadcast
title: IAMNetworkStatus::get_IsBroadcast (qnetwork.h)
description: The get_IsBroadcast method retrieves a value indicating whether the current stream is a broadcast stream.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_IsBroadcast method","IAMNetworkStatus.get_IsBroadcast","IAMNetworkStatus::get_IsBroadcast","IAMNetworkStatusget_IsBroadcast","dshow.iamnetworkstatus_get_isbroadcast","get_IsBroadcast","get_IsBroadcast method [DirectShow]","get_IsBroadcast method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_IsBroadcast"]
old-location: dshow\iamnetworkstatus_get_isbroadcast.htm
tech.root: dshow
ms.assetid: 578fe82b-0c87-47ea-9600-91d68f4c733f
ms.date: 4/26/2023
ms.keywords: IAMNetworkStatus interface [DirectShow],get_IsBroadcast method, IAMNetworkStatus.get_IsBroadcast, IAMNetworkStatus::get_IsBroadcast, IAMNetworkStatusget_IsBroadcast, dshow.iamnetworkstatus_get_isbroadcast, get_IsBroadcast, get_IsBroadcast method [DirectShow], get_IsBroadcast method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_IsBroadcast
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
 - IAMNetworkStatus::get_IsBroadcast
 - qnetwork/IAMNetworkStatus::get_IsBroadcast
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
 - IAMNetworkStatus.get_IsBroadcast
---

# IAMNetworkStatus::get_IsBroadcast


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_IsBroadcast</code> method retrieves a value indicating whether the current stream is a broadcast stream.

## -parameters

### -param pIsBroadcast

Pointer to a variable that receives a Boolean value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

A broadcast stream can be unicast or multicast. In a broadcast connection, the client is passive and does not control when the stream starts or stops. In an on-demand connection, the client is active and controls when the stream is started and stopped.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>