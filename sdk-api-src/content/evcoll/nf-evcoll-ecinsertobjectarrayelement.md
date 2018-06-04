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

# EcInsertObjectArrayElement function


## -description


The <b>EcInsertObjectArrayElement</b> function inserts an empty object into an array of property values for the event sources of a subscription. The object is inserted at a specified array index.


## -parameters




### -param ObjectArray [in]

A  handle to the array in which the object is inserted into. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.


### -param ArrayIndex [in]

An array index indicating where to insert the object.


## -returns



This function returns BOOL.




## -remarks



Arrays are zero-based, so the index for the first item in the array is 0.

Use the <a href="https://msdn.microsoft.com/0c219e3b-a7dd-4a7f-8fb3-0d281351ba24">EcSetObjectArrayProperty</a> to set individual properties of an empty object inserted into the array specified in the <i>ObjectArray</i> parameter.


#### Examples

For example code using the <b>EcInsertObjectArrayElement</b> function, see <a href="https://msdn.microsoft.com/f0100938-1702-4ef7-b20e-a0e8df224d18">Adding an Event Source to a Collector Initiated Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

