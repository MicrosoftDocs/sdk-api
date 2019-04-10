---
UID: NF:comsvcs.IGetAppTrackerData.GetTrackerDataAsCollectionObject
title: IGetAppTrackerData::GetTrackerDataAsCollectionObject (comsvcs.h)
author: windows-sdk-content
description: Retrieves tracking data for all COM+ applications in the form of a collection object.
old-location: cos\igetapptrackerdata_gettrackerdataascollectionobject.htm
tech.root: cossdk
ms.assetid: 215523ad-5f18-4529-8b23-afbd1b738fb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTrackerDataAsCollectionObject, GetTrackerDataAsCollectionObject method [COM+], GetTrackerDataAsCollectionObject method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetTrackerDataAsCollectionObject method, IGetAppTrackerData.GetTrackerDataAsCollectionObject, IGetAppTrackerData::GetTrackerDataAsCollectionObject, comsvcs/IGetAppTrackerData::GetTrackerDataAsCollectionObject, cos.igetapptrackerdata_gettrackerdataascollectionobject
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetAppTrackerData.GetTrackerDataAsCollectionObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

