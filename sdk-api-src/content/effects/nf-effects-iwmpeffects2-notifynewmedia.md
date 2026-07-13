---
UID: NF:effects.IWMPEffects2.NotifyNewMedia
title: IWMPEffects2::NotifyNewMedia (effects.h)
description: The NotifyNewMedia method is called by Windows Media Player to inform the visualization that a new media item has been loaded.
helpviewer_keywords: ["IWMPEffects2 interface [Windows Media Player]","NotifyNewMedia method","IWMPEffects2.NotifyNewMedia","IWMPEffects2::NotifyNewMedia","IWMPEffectsNotifyNewMedia","NotifyNewMedia","NotifyNewMedia method [Windows Media Player]","NotifyNewMedia method [Windows Media Player]","IWMPEffects2 interface","effects/IWMPEffects2::NotifyNewMedia","wmp.iwmpeffects2_notifynewmedia"]
old-location: wmp\iwmpeffects2_notifynewmedia.htm
tech.root: WMP
ms.assetid: ad1082af-9cba-4427-bacb-e552910f8e16
ms.date: 4/26/2023
ms.keywords: IWMPEffects2 interface [Windows Media Player],NotifyNewMedia method, IWMPEffects2.NotifyNewMedia, IWMPEffects2::NotifyNewMedia, IWMPEffectsNotifyNewMedia, NotifyNewMedia, NotifyNewMedia method [Windows Media Player], NotifyNewMedia method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::NotifyNewMedia, wmp.iwmpeffects2_notifynewmedia
req.header: effects.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEffects2::NotifyNewMedia
 - effects/IWMPEffects2::NotifyNewMedia
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects2.NotifyNewMedia
---

# IWMPEffects2::NotifyNewMedia


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>NotifyNewMedia</b> method is called by Windows Media Player to inform the visualization that a new media item has been loaded.

## -parameters

### -param pMedia [in]

Pointer to an <b>IWMPMedia</b> interface that represents the new media item.

## -returns

This method returns an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>