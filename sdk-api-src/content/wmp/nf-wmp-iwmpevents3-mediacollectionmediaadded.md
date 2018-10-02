---
UID: NF:wmp.IWMPEvents3.MediaCollectionMediaAdded
title: IWMPEvents3::MediaCollectionMediaAdded
author: windows-sdk-content
description: The MediaCollectionMediaAdded event occurs when a media item is added to the local library.
old-location: wmp\iwmpevents3_iwmpevents3__mediacollectionmediaadded.htm
tech.root: WMP
ms.assetid: 374ac1d8-ea7f-498a-b9b1-02bf7083f682
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPEvents3 interface [Windows Media Player],MediaCollectionMediaAdded method, IWMPEvents3.MediaCollectionMediaAdded, IWMPEvents3::MediaCollectionMediaAdded, IWMPEvents3MediaCollectionMediaAdded, MediaCollectionMediaAdded, MediaCollectionMediaAdded method [Windows Media Player], MediaCollectionMediaAdded method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__mediacollectionmediaadded, wmp/IWMPEvents3::MediaCollectionMediaAdded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.MediaCollectionMediaAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents3::MediaCollectionMediaAdded


## -description



The <b>MediaCollectionMediaAdded</b> event occurs when a media item is added to the local library.




## -parameters




### -param pdispMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item added to the local library. Call <b>QueryInterface</b> to retrieve a pointer to <b>IWMPMedia</b>.


## -returns



This method does not return a value.




## -remarks



This event occurs only for the local library.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

