---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringAdded
title: IWMPEvents::MediaCollectionAttributeStringAdded (wmp.h)
description: The MediaCollectionAttributeStringAdded event occurs when an attribute is added to the library.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","MediaCollectionAttributeStringAdded method","IWMPEvents.MediaCollectionAttributeStringAdded","IWMPEvents::MediaCollectionAttributeStringAdded","IWMPEventsMediaCollectionAttributeStringAdded","MediaCollectionAttributeStringAdded","MediaCollectionAttributeStringAdded method [Windows Media Player]","MediaCollectionAttributeStringAdded method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__mediacollectionattributestringadded","wmp/IWMPEvents::MediaCollectionAttributeStringAdded"]
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringadded.htm
tech.root: WMP
ms.assetid: c18aa7d1-2788-473d-8ade-5e897b83a4d6
ms.date: 12/05/2018
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