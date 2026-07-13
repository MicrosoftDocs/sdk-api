---
UID: NF:wmp.IWMPEvents3.MediaCollectionMediaAdded
title: IWMPEvents3::MediaCollectionMediaAdded (wmp.h)
description: The MediaCollectionMediaAdded event occurs when a media item is added to the local library.
helpviewer_keywords: ["IWMPEvents3 interface [Windows Media Player]","MediaCollectionMediaAdded method","IWMPEvents3.MediaCollectionMediaAdded","IWMPEvents3::MediaCollectionMediaAdded","IWMPEvents3MediaCollectionMediaAdded","MediaCollectionMediaAdded","MediaCollectionMediaAdded method [Windows Media Player]","MediaCollectionMediaAdded method [Windows Media Player]","IWMPEvents3 interface","wmp.iwmpevents3_iwmpevents3__mediacollectionmediaadded","wmp/IWMPEvents3::MediaCollectionMediaAdded"]
old-location: wmp\iwmpevents3_iwmpevents3__mediacollectionmediaadded.htm
tech.root: WMP
ms.assetid: 374ac1d8-ea7f-498a-b9b1-02bf7083f682
ms.date: 4/26/2023
ms.keywords: IWMPEvents3 interface [Windows Media Player],MediaCollectionMediaAdded method, IWMPEvents3.MediaCollectionMediaAdded, IWMPEvents3::MediaCollectionMediaAdded, IWMPEvents3MediaCollectionMediaAdded, MediaCollectionMediaAdded, MediaCollectionMediaAdded method [Windows Media Player], MediaCollectionMediaAdded method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__mediacollectionmediaadded, wmp/IWMPEvents3::MediaCollectionMediaAdded
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPEvents3::MediaCollectionMediaAdded
 - wmp/IWMPEvents3::MediaCollectionMediaAdded
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
 - IWMPEvents3.MediaCollectionMediaAdded
---

# IWMPEvents3::MediaCollectionMediaAdded


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MediaCollectionMediaAdded</b> event occurs when a media item is added to the local library.

## -parameters

### -param pdispMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item added to the local library. Call <b>QueryInterface</b> to retrieve a pointer to <b>IWMPMedia</b>.

## -remarks

This event occurs only for the local library.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>