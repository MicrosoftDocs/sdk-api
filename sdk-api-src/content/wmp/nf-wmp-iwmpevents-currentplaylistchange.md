---
UID: NF:wmp.IWMPEvents.CurrentPlaylistChange
title: IWMPEvents::CurrentPlaylistChange (wmp.h)
description: The CurrentPlaylistChange event occurs when something changes within the current playlist.
helpviewer_keywords: ["CurrentPlaylistChange","CurrentPlaylistChange method [Windows Media Player]","CurrentPlaylistChange method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","CurrentPlaylistChange method","IWMPEvents.CurrentPlaylistChange","IWMPEvents::CurrentPlaylistChange","IWMPEventsCurrentPlaylistChange","wmp.iwmpevents_iwmpevents__currentplaylistchange","wmp/IWMPEvents::CurrentPlaylistChange"]
old-location: wmp\iwmpevents_iwmpevents__currentplaylistchange.htm
tech.root: WMP
ms.assetid: b8020b8a-4f2e-4039-862e-9c0f371645fa
ms.date: 12/05/2018
ms.keywords: CurrentPlaylistChange, CurrentPlaylistChange method [Windows Media Player], CurrentPlaylistChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentPlaylistChange method, IWMPEvents.CurrentPlaylistChange, IWMPEvents::CurrentPlaylistChange, IWMPEventsCurrentPlaylistChange, wmp.iwmpevents_iwmpevents__currentplaylistchange, wmp/IWMPEvents::CurrentPlaylistChange
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
 - IWMPEvents::CurrentPlaylistChange
 - wmp/IWMPEvents::CurrentPlaylistChange
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
 - IWMPEvents.CurrentPlaylistChange
---

# IWMPEvents::CurrentPlaylistChange


## -description

The <b>CurrentPlaylistChange</b> event occurs when something changes within the current playlist.

## -parameters

### -param change [in]

Specifies what type of change occurred to the playlist. See the <b>PlaylistChange</b> event for a table of possible values.

## -remarks

This event does not occur when a different playlist becomes the current playlist. It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-playlistchange">PlaylistChange</a>