---
UID: NF:wmp.IWMPEvents.PlayStateChange
title: IWMPEvents::PlayStateChange (wmp.h)
description: The PlayStateChange event occurs when the play state of the Windows Media Player control changes.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PlayStateChange method","IWMPEvents.PlayStateChange","IWMPEvents::PlayStateChange","IWMPEventsPlayStateChange","PlayStateChange","PlayStateChange method [Windows Media Player]","PlayStateChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__playstatechange","wmp/IWMPEvents::PlayStateChange"]
old-location: wmp\iwmpevents_iwmpevents__playstatechange.htm
tech.root: WMP
ms.assetid: d7bd4fde-8b08-4450-b291-1249393b5388
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PlayStateChange method, IWMPEvents.PlayStateChange, IWMPEvents::PlayStateChange, IWMPEventsPlayStateChange, PlayStateChange, PlayStateChange method [Windows Media Player], PlayStateChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__playstatechange, wmp/IWMPEvents::PlayStateChange
f1_keywords:
- wmp/IWMPEvents.PlayStateChange
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
- IWMPEvents.PlayStateChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents::PlayStateChange


## -description



The <b>PlayStateChange</b> event occurs when the play state of the Windows Media Player control changes.




## -parameters




### -param NewState [in]

Specifies the new state.


## -remarks



Windows Media Player states are not guaranteed to occur in any particular order. Furthermore, not every state necessarily occurs during a sequence of events. You should not write code that relies upon state order.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>
 

 

