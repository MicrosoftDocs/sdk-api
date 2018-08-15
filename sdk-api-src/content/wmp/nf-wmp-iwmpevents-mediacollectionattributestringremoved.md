---
UID: NF:wmp.IWMPEvents.MediaCollectionAttributeStringRemoved
title: IWMPEvents::MediaCollectionAttributeStringRemoved
author: windows-sdk-content
description: The MediaCollectionAttributeStringRemoved event occurs when an attribute is removed from the library.
old-location: wmp\iwmpevents_iwmpevents__mediacollectionattributestringremoved.htm
old-project: WMP
ms.assetid: 4e7a3d71-4ec1-4c33-9101-d9d90ee8b1f9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPEvents interface [Windows Media Player],MediaCollectionAttributeStringRemoved method, IWMPEvents.MediaCollectionAttributeStringRemoved, IWMPEvents::MediaCollectionAttributeStringRemoved, IWMPEventsMediaCollectionAttributeStringRemoved, MediaCollectionAttributeStringRemoved, MediaCollectionAttributeStringRemoved method [Windows Media Player], MediaCollectionAttributeStringRemoved method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediacollectionattributestringremoved, wmp/IWMPEvents::MediaCollectionAttributeStringRemoved
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.MediaCollectionAttributeStringRemoved
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::MediaCollectionAttributeStringRemoved


## -description



The <b>MediaCollectionAttributeStringRemoved</b> event occurs when an attribute is removed from the library.




## -parameters




### -param bstrAttribName [in]

Specifies the name of the attribute. For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>.


### -param bstrAttribVal [in]

Specifies the value of the attribute.


## -returns



This method does not return a value.




## -remarks



When a media item is removed from the library, its metadata is removed from the <b>MediaCollection</b> object and this event is fired for each attribute that is removed.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

