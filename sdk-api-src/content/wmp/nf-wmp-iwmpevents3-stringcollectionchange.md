---
UID: NF:wmp.IWMPEvents3.StringCollectionChange
title: IWMPEvents3::StringCollectionChange
author: windows-sdk-content
description: The StringCollectionChange event occurs when a string collection changes.
old-location: wmp\iwmpevents3_iwmpevents3__stringcollectionchange.htm
tech.root: WMP
ms.assetid: 93880116-e354-49d0-ba02-391fbb4d3f8c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPEvents3 interface [Windows Media Player],StringCollectionChange method, IWMPEvents3.StringCollectionChange, IWMPEvents3::StringCollectionChange, IWMPEvents3StringCollectionChange, StringCollectionChange, StringCollectionChange method [Windows Media Player], StringCollectionChange method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__stringcollectionchange, wmp/IWMPEvents3::StringCollectionChange
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
 - IWMPEvents3.StringCollectionChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents3::StringCollectionChange


## -description



The <b>StringCollectionChange</b> event occurs when a string collection changes.




## -parameters




### -param pdispStringCollection [in]

Pointer to the <b>IDispatch</b> interface that represents the string collection that changed. Call <b>QueryInterface</b> to retrieve a pointer to <b>IWMPStringCollection</b>.


### -param change [in]


<a href="https://msdn.microsoft.com/7690972b-52ac-4249-baa5-3d2b38a4487a">WMPStringCollectionChangeEventType</a> value indicating the type of change that occurred.


### -param lCollectionIndex [in]

The index of the string collection item that changed.


## -returns



This method does not return a value.




## -remarks



To receive <b>StringCollectionChange</b> events, you must obtain your string collection as follows:

<ol>
<li>Call <a href="https://msdn.microsoft.com/6de39a4e-fcce-401b-9bbf-7b06d1fb0370">IWMPLibrary::get_mediaCollection</a> to get an <b>IWMPMediaCollection</b> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/c3699acb-58a1-4efa-a42c-c84534abca96">getAttributeStringCollection</a> method of the interface you obtained in step 1.</li>
</ol>
If you obtain your <b>IWMPMediaCollection</b> interface by calling <a href="https://msdn.microsoft.com/41b090ca-edf0-440e-b578-26c5ad064657">IWMPCore::get_mediaCollection</a>, you will not receive <b>StringCollectionChange</b> events.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/8cdabea9-7e37-4e63-9d6c-b6f63aa536ea">IWMPStringCollection Interface</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

