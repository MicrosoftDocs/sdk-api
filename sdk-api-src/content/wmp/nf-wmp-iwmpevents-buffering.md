---
UID: NF:wmp.IWMPEvents.Buffering
title: IWMPEvents::Buffering
author: windows-sdk-content
description: The Buffering event occurs when the Windows Media Player control begins or ends buffering.
old-location: wmp\iwmpevents_iwmpevents__buffering.htm
tech.root: WMP
ms.assetid: 3e379c92-b400-48ad-a3d3-82ed3cd3f396
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Buffering, Buffering method [Windows Media Player], Buffering method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],Buffering method, IWMPEvents.Buffering, IWMPEvents::Buffering, IWMPEventsBuffering, wmp.iwmpevents_iwmpevents__buffering, wmp/IWMPEvents::Buffering
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::Buffering


## -description



The <b>Buffering</b> event occurs when the Windows Media Player control begins or ends buffering.




## -parameters




### -param Start [in]

Specifies whether buffering has begun or ended. A value of true indicates that it has begun; a value of false indicates that it has ended.


## -returns



This method does not return a value.




## -remarks



Use this event to determine when buffering or downloading starts or stops. You can use the same event block for both cases and test <b>IWMPNetwork::get_bufferingProgress</b> and <b>IWMPNetwork::get_downloadProgress</b> to determine whether Windows Media Player is currently buffering or downloading content.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/5c8cc541-3fc2-49b8-8a1a-f4959989aafe">IWMPNetwork::get_bufferingProgress</a>



<a href="https://msdn.microsoft.com/e9ed2027-cba4-4701-a416-a2190b51570c">IWMPNetwork::get_downloadProgress</a>
 

 

