---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringRemoved
title: IWMPEvents::MediaCollectionAttributeStringRemoved (wmp.h)
description: The MediaCollectionAttributeStringRemoved event occurs when an attribute is removed from the library.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","MediaCollectionAttributeStringRemoved method","IWMPEvents.MediaCollectionAttributeStringRemoved","IWMPEvents::MediaCollectionAttributeStringRemoved","IWMPEventsMediaCollectionAttributeStringRemoved","MediaCollectionAttributeStringRemoved","MediaCollectionAttributeStringRemoved method [Windows Media Player]","MediaCollectionAttributeStringRemoved method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__mediacollectionattributestringremoved","wmp/IWMPEvents::MediaCollectionAttributeStringRemoved"]
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringremoved.htm
tech.root: WMP
ms.assetid: 4e7a3d71-4ec1-4c33-9101-d9d90ee8b1f9
ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],MediaCollectionAttributeStringRemoved method, IWMPEvents.MediaCollectionAttributeStringRemoved, IWMPEvents::MediaCollectionAttributeStringRemoved, IWMPEventsMediaCollectionAttributeStringRemoved, MediaCollectionAttributeStringRemoved, MediaCollectionAttributeStringRemoved method [Windows Media Player], MediaCollectionAttributeStringRemoved method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediacollectionattributestringremoved, wmp/IWMPEvents::MediaCollectionAttributeStringRemoved
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
 - IWMPEvents::MediaCollectionAttributeStringRemoved
 - wmp/IWMPEvents::MediaCollectionAttributeStringRemoved
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
 - IWMPEvents.MediaCollectionAttributeStringRemoved
---

# IWMPEvents::MediaCollectionAttributeStringRemoved


## -description

The <b>MediaCollectionAttributeStringRemoved</b> event occurs when an attribute is removed from the library.

## -parameters

### -param bstrAttribName [in]

Specifies the name of the attribute. For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.

### -param bstrAttribVal [in]

Specifies the value of the attribute.

## -remarks

When a media item is removed from the library, its metadata is removed from the <b>MediaCollection</b> object and this event is fired for each attribute that is removed.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>