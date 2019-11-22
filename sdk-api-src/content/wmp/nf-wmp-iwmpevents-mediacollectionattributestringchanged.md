---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringChanged
title: IWMPEvents::MediaCollectionAttributeStringChanged (wmp.h)

description: The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringchanged.htm
tech.root: WMP
ms.assetid: 76767c3d-4dc1-4964-a337-6cde8f4c8609

ms.date: 12/05/2018
ms.keywords: IWMPEvents interface [Windows Media Player],MediaCollectionAttributeStringChanged method, IWMPEvents.MediaCollectionAttributeStringChanged, IWMPEvents::MediaCollectionAttributeStringChanged, IWMPEventsMediaCollectionAttributeStringChanged, MediaCollectionAttributeStringChanged, MediaCollectionAttributeStringChanged method [Windows Media Player], MediaCollectionAttributeStringChanged method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediacollectionattributestringchanged, wmp/IWMPEvents::MediaCollectionAttributeStringChanged
ms.topic: method
f1_keywords: 
 - "wmp/IWMPEvents.MediaCollectionAttributeStringChanged"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.MediaCollectionAttributeStringChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents::MediaCollectionAttributeStringChanged


## -description



The <b>MediaCollectionAttributeStringChanged</b> event occurs when an attribute value in the library is changed.




## -parameters




### -param bstrAttribName [in]

Specifies the name of the attribute. For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://docs.microsoft.com/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.


### -param bstrOldAttribVal [in]

Specifies the original attribute value.


### -param bstrNewAttribVal [in]

Specifies the new attribute value.


## -returns



This method does not return a value.




## -remarks



When a user modifies library metadata, the <b>MediaCollection</b> object is updated and this event fires for each attribute changed.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>
 

 

