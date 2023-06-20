---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringAdded
title: IWMPEvents::MediaCollectionAttributeStringAdded (wmp.h)
description: The MediaCollectionAttributeStringAdded event occurs when an attribute is added to the library.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","MediaCollectionAttributeStringAdded method","IWMPEvents.MediaCollectionAttributeStringAdded","IWMPEvents::MediaCollectionAttributeStringAdded","IWMPEventsMediaCollectionAttributeStringAdded","MediaCollectionAttributeStringAdded","MediaCollectionAttributeStringAdded method [Windows Media Player]","MediaCollectionAttributeStringAdded method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__mediacollectionattributestringadded","wmp/IWMPEvents::MediaCollectionAttributeStringAdded"]
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringadded.htm
tech.root: WMP
ms.assetid: c18aa7d1-2788-473d-8ade-5e897b83a4d6
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],MediaCollectionAttributeStringAdded method, IWMPEvents.MediaCollectionAttributeStringAdded, IWMPEvents::MediaCollectionAttributeStringAdded, IWMPEventsMediaCollectionAttributeStringAdded, MediaCollectionAttributeStringAdded, MediaCollectionAttributeStringAdded method [Windows Media Player], MediaCollectionAttributeStringAdded method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediacollectionattributestringadded, wmp/IWMPEvents::MediaCollectionAttributeStringAdded
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
 - IWMPEvents::MediaCollectionAttributeStringAdded
 - wmp/IWMPEvents::MediaCollectionAttributeStringAdded
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
 - IWMPEvents.MediaCollectionAttributeStringAdded
---

# IWMPEvents::MediaCollectionAttributeStringAdded


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MediaCollectionAttributeStringAdded</b> event occurs when an attribute is added to the library.

## -parameters

### -param bstrAttribName [in]

Specifies the attribute name. For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.

### -param bstrAttribVal [in]

Specifies the attribute value.

## -remarks

When a media item is added to the library, its metadata is added to the <b>MediaCollection</b> object and this event is fired for each attribute added.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>