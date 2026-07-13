---
UID: NF:qnetwork.IAMNetworkStatus.get_ReceivedPackets
title: IAMNetworkStatus::get_ReceivedPackets (qnetwork.h)
description: The get_ReceivedPackets method retrieves the number of packets that have been received.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_ReceivedPackets method","IAMNetworkStatus.get_ReceivedPackets","IAMNetworkStatus::get_ReceivedPackets","IAMNetworkStatusget_ReceivedPackets","dshow.iamnetworkstatus_get_receivedpackets","get_ReceivedPackets","get_ReceivedPackets method [DirectShow]","get_ReceivedPackets method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_ReceivedPackets"]
old-location: dshow\iamnetworkstatus_get_receivedpackets.htm
tech.root: dshow
ms.assetid: 9437489d-87bf-45d4-82f3-22e8adb4df54
ms.date: 4/26/2023
ms.keywords: IAMNetworkStatus interface [DirectShow],get_ReceivedPackets method, IAMNetworkStatus.get_ReceivedPackets, IAMNetworkStatus::get_ReceivedPackets, IAMNetworkStatusget_ReceivedPackets, dshow.iamnetworkstatus_get_receivedpackets, get_ReceivedPackets, get_ReceivedPackets method [DirectShow], get_ReceivedPackets method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_ReceivedPackets
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
 - IAMNetworkStatus::get_ReceivedPackets
 - qnetwork/IAMNetworkStatus::get_ReceivedPackets
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
 - IAMNetworkStatus.get_ReceivedPackets
---

# IAMNetworkStatus::get_ReceivedPackets


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ReceivedPackets</code> method retrieves the number of packets that have been received.

## -parameters

### -param pReceivedPackets

Pointer to a variable that receives the number of received packets.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>