---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringAdded
title: IWMPEvents::MediaCollectionAttributeStringAdded (wmp.h)
author: windows-sdk-content
description: The MediaCollectionAttributeStringAdded event occurs when an attribute is added to the library.
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringadded.htm
tech.root: WMP
ms.assetid: c18aa7d1-2788-473d-8ade-5e897b83a4d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPEvents interface [Windows Media Player],MediaCollectionAttributeStringAdded method, IWMPEvents.MediaCollectionAttributeStringAdded, IWMPEvents::MediaCollectionAttributeStringAdded, IWMPEventsMediaCollectionAttributeStringAdded, MediaCollectionAttributeStringAdded, MediaCollectionAttributeStringAdded method [Windows Media Player], MediaCollectionAttributeStringAdded method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediacollectionattributestringadded, wmp/IWMPEvents::MediaCollectionAttributeStringAdded
ms.topic: method
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
 - IWMPEvents.MediaCollectionAttributeStringAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents::MediaCollectionAttributeStringAdded


## -description



The <b>MediaCollectionAttributeStringAdded</b> event occurs when an attribute is added to the library.




## -parameters




### -param bstrAttribName [in]

Specifies the attribute name. For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>.


### -param bstrAttribVal [in]

Specifies the attribute value.


## -returns



This method does not return a value.




## -remarks



When a media item is added to the library, its metadata is added to the <b>MediaCollection</b> object and this event is fired for each attribute added.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563310(v=VS.85).aspx">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563405(v=VS.85).aspx">IWMPMediaCollection Interface</a>
 

 

