---
UID: NF:wmp.IWMPEvents.CurrentMediaItemAvailable
title: IWMPEvents::CurrentMediaItemAvailable (wmp.h)
description: The CurrentMediaItemAvailable event occurs when the current media item becomes available.
helpviewer_keywords: ["CurrentMediaItemAvailable","CurrentMediaItemAvailable method [Windows Media Player]","CurrentMediaItemAvailable method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","CurrentMediaItemAvailable method","IWMPEvents.CurrentMediaItemAvailable","IWMPEvents::CurrentMediaItemAvailable","IWMPEventsCurrentMediaItemAvailable","wmp.iwmpevents_iwmpevents__currentmediaitemavailable","wmp/IWMPEvents::CurrentMediaItemAvailable"]
old-location: wmp\iwmpevents_iwmpevents__currentmediaitemavailable.htm
tech.root: WMP
ms.assetid: 8e6e92b7-1916-4628-915b-e9ee0d52fe75
ms.date: 4/26/2023
ms.keywords: CurrentMediaItemAvailable, CurrentMediaItemAvailable method [Windows Media Player], CurrentMediaItemAvailable method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],CurrentMediaItemAvailable method, IWMPEvents.CurrentMediaItemAvailable, IWMPEvents::CurrentMediaItemAvailable, IWMPEventsCurrentMediaItemAvailable, wmp.iwmpevents_iwmpevents__currentmediaitemavailable, wmp/IWMPEvents::CurrentMediaItemAvailable
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
 - IWMPEvents::CurrentMediaItemAvailable
 - wmp/IWMPEvents::CurrentMediaItemAvailable
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
 - IWMPEvents.CurrentMediaItemAvailable
---

# IWMPEvents::CurrentMediaItemAvailable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CurrentMediaItemAvailable</b> event occurs when the current media item becomes available.

## -parameters

### -param bstrItemName [in]

Specifies the item name.

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>