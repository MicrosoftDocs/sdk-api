---
UID: NF:wmp.IWMPEvents.Buffering
title: IWMPEvents::Buffering (wmp.h)
description: The Buffering event occurs when the Windows Media Player control begins or ends buffering.helpviewer_keywords: ["Buffering","Buffering method [Windows Media Player]","Buffering method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","Buffering method","IWMPEvents.Buffering","IWMPEvents::Buffering","IWMPEventsBuffering","wmp.iwmpevents_iwmpevents__buffering","wmp/IWMPEvents::Buffering"]
old-location: wmp\iwmpevents_iwmpevents__buffering.htm
tech.root: WMP
ms.assetid: 3e379c92-b400-48ad-a3d3-82ed3cd3f396
ms.date: 12/05/2018
ms.keywords: Buffering, Buffering method [Windows Media Player], Buffering method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],Buffering method, IWMPEvents.Buffering, IWMPEvents::Buffering, IWMPEventsBuffering, wmp.iwmpevents_iwmpevents__buffering, wmp/IWMPEvents::Buffering
f1_keywords:
- wmp/IWMPEvents.Buffering
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPEvents.Buffering
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents::Buffering


## -description



The <b>Buffering</b> event occurs when the Windows Media Player control begins or ends buffering.




## -parameters




### -param Start [in]

Specifies whether buffering has begun or ended. A value of true indicates that it has begun; a value of false indicates that it has ended.


## -remarks



Use this event to determine when buffering or downloading starts or stops. You can use the same event block for both cases and test <b>IWMPNetwork::get_bufferingProgress</b> and <b>IWMPNetwork::get_downloadProgress</b> to determine whether Windows Media Player is currently buffering or downloading content.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_bufferingprogress">IWMPNetwork::get_bufferingProgress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-get_downloadprogress">IWMPNetwork::get_downloadProgress</a>
 

 

