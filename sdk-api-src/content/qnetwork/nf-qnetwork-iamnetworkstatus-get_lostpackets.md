---
UID: NF:qnetwork.IAMNetworkStatus.get_LostPackets
title: IAMNetworkStatus::get_LostPackets (qnetwork.h)
description: The get_LostPackets method retrieves the number of packets that have been lost.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_LostPackets method","IAMNetworkStatus.get_LostPackets","IAMNetworkStatus::get_LostPackets","IAMNetworkStatusget_LostPackets","dshow.iamnetworkstatus_get_lostpackets","get_LostPackets","get_LostPackets method [DirectShow]","get_LostPackets method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_LostPackets"]
old-location: dshow\iamnetworkstatus_get_lostpackets.htm
tech.root: dshow
ms.assetid: 814a2ffa-c7f3-47e6-8956-4a705b394469
ms.date: 4/26/2023
ms.keywords: IAMNetworkStatus interface [DirectShow],get_LostPackets method, IAMNetworkStatus.get_LostPackets, IAMNetworkStatus::get_LostPackets, IAMNetworkStatusget_LostPackets, dshow.iamnetworkstatus_get_lostpackets, get_LostPackets, get_LostPackets method [DirectShow], get_LostPackets method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_LostPackets
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
 - IAMNetworkStatus::get_LostPackets
 - qnetwork/IAMNetworkStatus::get_LostPackets
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
 - IAMNetworkStatus.get_LostPackets
---

# IAMNetworkStatus::get_LostPackets


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_LostPackets</code> method retrieves the number of packets that have been lost.

## -parameters

### -param pLostPackets

Pointer to a variable that receives the number of lost packets.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless. Packets may be lost for a number of reasons, such as the type and quality of the network connection.

Whenever playback is stopped and restarted, this property is set to zero. It is not reset if playback is paused and restarted.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>