---
UID: NF:wmp.IWMPEvents.DoubleClick
title: IWMPEvents::DoubleClick (wmp.h)
description: The DoubleClick event occurs when the user double-clicks a mouse button.
helpviewer_keywords: ["DoubleClick","DoubleClick method [Windows Media Player]","DoubleClick method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","DoubleClick method","IWMPEvents.DoubleClick","IWMPEvents::DoubleClick","IWMPEventsDoubleClick","wmp.iwmpevents_iwmpevents__doubleclick","wmp/IWMPEvents::DoubleClick"]
old-location: wmp\iwmpevents_iwmpevents__doubleclick.htm
tech.root: WMP
ms.assetid: 76b1eebb-45d9-40fc-a845-24a7dac8c96c
ms.date: 4/26/2023
ms.keywords: DoubleClick, DoubleClick method [Windows Media Player], DoubleClick method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],DoubleClick method, IWMPEvents.DoubleClick, IWMPEvents::DoubleClick, IWMPEventsDoubleClick, wmp.iwmpevents_iwmpevents__doubleclick, wmp/IWMPEvents::DoubleClick
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
 - IWMPEvents::DoubleClick
 - wmp/IWMPEvents::DoubleClick
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
 - IWMPEvents.DoubleClick
---

# IWMPEvents::DoubleClick


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DoubleClick</b> event occurs when the user double-clicks a mouse button.

## -parameters

### -param nButton [in]

A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2). These bits correspond to the values 1, 2, and 4, respectively. Only one of the bits is set, indicating the button that caused the event.

### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.

### -param fX [in]

The x coordinate of the mouse pointer relative to the upper left-hand corner of the control.

### -param fY [in]

The y coordinate of the mouse pointer relative to the upper left-hand corner of the control.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>