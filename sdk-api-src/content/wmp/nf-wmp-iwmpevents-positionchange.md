---
UID: NF:wmp.IWMPEvents.PositionChange
title: IWMPEvents::PositionChange (wmp.h)
description: The PositionChange event occurs when the current playback position within the media item has been changed.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","PositionChange method","IWMPEvents.PositionChange","IWMPEvents::PositionChange","IWMPEventsPositionChange","PositionChange","PositionChange method [Windows Media Player]","PositionChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__positionchange","wmp/IWMPEvents::PositionChange"]
old-location: wmp\iwmpevents_iwmpevents__positionchange.htm
tech.root: WMP
ms.assetid: 644aaab0-8028-4dd2-9f56-f97db2b22d69
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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