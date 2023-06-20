---
UID: NF:wmp.IWMPEvents.CurrentPlaylistItemAvailable
title: IWMPEvents::CurrentPlaylistItemAvailable (wmp.h)
description: The CurrentPlaylistItemAvailable event occurs when the current playlist item becomes available.
helpviewer_keywords: ["CurrentPlaylistItemAvailable","CurrentPlaylistItemAvailable method [Windows Media Player]","CurrentPlaylistItemAvailable method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","CurrentPlaylistItemAvailable method","IWMPEvents.CurrentPlaylistItemAvailable","IWMPEvents::CurrentPlaylistItemAvailable","IWMPEventsCurrentPlaylistItemAvailable","wmp.iwmpevents_iwmpevents__currentplaylistitemavailable","wmp/IWMPEvents::CurrentPlaylistItemAvailable"]
old-location: wmp\iwmpevents_iwmpevents__currentplaylistitemavailable.htm
tech.root: WMP
ms.assetid: 77209df0-3b3d-4fc8-b560-a2c02138e746
ms.date: 4/26/2023
ms.keywords: CurrentPlaylistItemAvailable, CurrentPlaylistItemAvailable method [Windows Media Player], CurrentPlaylistItemAvailable method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentPlaylistItemAvailable method, IWMPEvents.CurrentPlaylistItemAvailable, IWMPEvents::CurrentPlaylistItemAvailable, IWMPEventsCurrentPlaylistItemAvailable, wmp.iwmpevents_iwmpevents__currentplaylistitemavailable, wmp/IWMPEvents::CurrentPlaylistItemAvailable
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
 - IWMPEvents::CurrentPlaylistItemAvailable
 - wmp/IWMPEvents::CurrentPlaylistItemAvailable
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
 - IWMPEvents.CurrentPlaylistItemAvailable
---

# IWMPEvents::CurrentPlaylistItemAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CurrentPlaylistItemAvailable</b> event occurs when the current playlist item becomes available.

## -parameters

### -param bstrItemName [in]

Specifies the item name.

## -remarks

The name of the current playlist can be used to retrieve the corresponding <b>Playlist</b> object by using the <b>IWMPPlaylistCollection::getByName</b> method.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>