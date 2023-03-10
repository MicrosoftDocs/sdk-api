---
UID: NF:wmp.IWMPEvents.KeyUp
title: IWMPEvents::KeyUp (wmp.h)
description: The KeyUp event occurs when a key is released.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","KeyUp method","IWMPEvents.KeyUp","IWMPEvents::KeyUp","IWMPEventsKeyUp","KeyUp","KeyUp method [Windows Media Player]","KeyUp method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__keyup","wmp/IWMPEvents::KeyUp"]
old-location: wmp\iwmpevents_iwmpevents__keyup.htm
tech.root: WMP
ms.assetid: e76e11d8-6cb9-488e-b5ca-1b5b11898d4b
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],KeyUp method, IWMPEvents.KeyUp, IWMPEvents::KeyUp, IWMPEventsKeyUp, KeyUp, KeyUp method [Windows Media Player], KeyUp method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__keyup, wmp/IWMPEvents::KeyUp
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
 - IWMPEvents::KeyUp
 - wmp/IWMPEvents::KeyUp
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
 - IWMPEvents.KeyUp
---

# IWMPEvents::KeyUp


## -description

The <b>KeyUp</b> event occurs when a key is released.

## -parameters

### -param nKeyCode [in]

Specifies which physical key is pressed. For possible values, see the Remarks section of the <b>KeyDown</b> event.

### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-keydown">KeyDown</a>