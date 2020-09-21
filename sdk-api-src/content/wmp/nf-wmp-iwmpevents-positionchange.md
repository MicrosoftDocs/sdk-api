---
UID: NF:wmp.IWMPEvents.PositionChange
title: IWMPEvents::PositionChange (wmp.h)
description: The PositionChange event occurs when the current playback position within the media item has been changed.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PositionChange method","IWMPEvents.PositionChange","IWMPEvents::PositionChange","IWMPEventsPositionChange","PositionChange","PositionChange method [Windows Media Player]","PositionChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__positionchange","wmp/IWMPEvents::PositionChange"]
old-location: wmp\iwmpevents_iwmpevents__positionchange.htm
tech.root: WMP
ms.assetid: 644aaab0-8028-4dd2-9f56-f97db2b22d69
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],PositionChange method, IWMPEvents.PositionChange, IWMPEvents::PositionChange, IWMPEventsPositionChange, PositionChange, PositionChange method [Windows Media Player], PositionChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__positionchange, wmp/IWMPEvents::PositionChange
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
 - IWMPEvents::PositionChange
 - wmp/IWMPEvents::PositionChange
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
 - IWMPEvents.PositionChange
---

# IWMPEvents::PositionChange


## -description

The <b>PositionChange</b> event occurs when the current playback position within the media item has been changed.

## -parameters

### -param oldPosition [in]

Specifies the original position.

### -param newPosition [in]

Specifies the new position.

## -remarks

This event is not raised routinely during playback. It only occurs when something actively changes the current playback position within the playing media item, such as the user moving the seek handle or code specifying a value for <b>IWMPControls::currentPosition</b>.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>