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

# IGetAppTrackerData::GetTrackerDataAsCollectionObject


## -description


Retrieves tracking data for all COM+ applications in the form of a collection object.


## -parameters




### -param TopLevelCollection [out]

On return, the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface for a collection of tracker data.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



This method is primarily intended to enable applications that subscribe to the <a href="https://msdn.microsoft.com/bed709ca-5083-4073-a9f9-2b7b7f14cf87">IComTrackingInfoEvents</a> event interface to add support for <a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a> with minimal changes to their code. The object returned by this method is identical to the object sent in calls to subscribers' <a href="https://msdn.microsoft.com/a63f6782-b50a-4457-bd51-4eba8c413a47">IComTrackingInfoEvent::OnNewTrackingInfo</a> method, so that code for navigating and parsing this collection may be reused. 



Applications should not expect this method to return newly updated tracking data any more frequently than the server's suggested polling interval (see <a href="https://msdn.microsoft.com/fcc65fd3-debf-4b5c-aaf2-3e7234510d35">IGetAppTrackerData::GetSuggestedPollingInterval</a>). 



Note that the collection object returned by this method does not contain all tracking data that is available by calling the other methods. In particular, recycling details and hang monitoring configuration are not provided. 





## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

