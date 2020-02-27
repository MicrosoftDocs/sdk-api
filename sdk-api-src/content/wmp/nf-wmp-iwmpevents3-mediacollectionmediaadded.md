---
UID: NF:wmp.IWMPEvents3.MediaCollectionMediaAdded
title: IWMPEvents3::MediaCollectionMediaAdded (wmp.h)
description: The MediaCollectionMediaAdded event occurs when a media item is added to the local library.
old-location: wmp\iwmpevents3_iwmpevents3__mediacollectionmediaadded.htm
tech.root: WMP
ms.assetid: 374ac1d8-ea7f-498a-b9b1-02bf7083f682
ms.date: 12/05/2018
ms.keywords: IWMPEvents3 interface [Windows Media Player],MediaCollectionMediaAdded method, IWMPEvents3.MediaCollectionMediaAdded, IWMPEvents3::MediaCollectionMediaAdded, IWMPEvents3MediaCollectionMediaAdded, MediaCollectionMediaAdded, MediaCollectionMediaAdded method [Windows Media Player], MediaCollectionMediaAdded method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__mediacollectionmediaadded, wmp/IWMPEvents3::MediaCollectionMediaAdded
f1_keywords:
- wmp/IWMPEvents3.MediaCollectionMediaAdded
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 

