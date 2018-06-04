---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 

