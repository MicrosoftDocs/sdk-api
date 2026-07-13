---
UID: NF:wmp.IWMPEvents.Buffering
title: IWMPEvents::Buffering (wmp.h)
description: The Buffering event occurs when the Windows Media Player control begins or ends buffering.
helpviewer_keywords: ["Buffering","Buffering method [Windows Media Player]","Buffering method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","Buffering method","IWMPEvents.Buffering","IWMPEvents::Buffering","IWMPEventsBuffering","wmp.iwmpevents_iwmpevents__buffering","wmp/IWMPEvents::Buffering"]
old-location: wmp\iwmpevents_iwmpevents__buffering.htm
tech.root: WMP
ms.assetid: 3e379c92-b400-48ad-a3d3-82ed3cd3f396
ms.date: 4/26/2023
ms.keywords: Buffering, Buffering method [Windows Media Player], Buffering method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],Buffering method, IWMPEvents.Buffering, IWMPEvents::Buffering, IWMPEventsBuffering, wmp.iwmpevents_iwmpevents__buffering, wmp/IWMPEvents::Buffering
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::Buffering
 - wmp/IWMPEvents::Buffering
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.Buffering
---

# IWMPEvents::Buffering


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Buffering</b> event occurs when the Windows Media Player control begins or ends buffering.

## -parameters

### -param Start [in]

Specifies whether buffering has begun or ended. A value of true indicates that it has begun; a value of false indicates that it has ended.

## -remarks

Use this event to determine when buffering or downloading starts or stops. You can use the same event block for both cases and test <b>IWMPNetwork::get_bufferingProgress</b> and <b>IWMPNetwork::get_downloadProgress</b> to determine whether Windows Media Player is currently buffering or downloading content.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingprogress">IWMPNetwork::get_bufferingProgress</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_downloadprogress">IWMPNetwork::get_downloadProgress</a>