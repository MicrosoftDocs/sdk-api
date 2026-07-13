---
UID: NF:wmp.IWMPEvents.MediaChange
title: IWMPEvents::MediaChange (wmp.h)
description: The MediaChange event occurs when a media item changes.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","MediaChange method","IWMPEvents.MediaChange","IWMPEvents::MediaChange","IWMPEventsMediaChange","MediaChange","MediaChange method [Windows Media Player]","MediaChange method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__mediachange","wmp/IWMPEvents::MediaChange"]
old-location: wmp\iwmpevents_iwmpevents__mediachange.htm
tech.root: WMP
ms.assetid: 385fb52c-62d2-482d-bc9f-94dbf693a27c
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],MediaChange method, IWMPEvents.MediaChange, IWMPEvents::MediaChange, IWMPEventsMediaChange, MediaChange, MediaChange method [Windows Media Player], MediaChange method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediachange, wmp/IWMPEvents::MediaChange
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
 - IWMPEvents::MediaChange
 - wmp/IWMPEvents::MediaChange
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
 - IWMPEvents.MediaChange
---

# IWMPEvents::MediaChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MediaChange</b> event occurs when a media item changes.

## -parameters

### -param Item [in]

Pointer to an <b>IDispatch</b> interface that identifies the item that changed.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>