---
UID: NF:comsvcs.IGetAppTrackerData.GetTrackerDataAsCollectionObject
title: IGetAppTrackerData::GetTrackerDataAsCollectionObject (comsvcs.h)
description: Retrieves tracking data for all COM+ applications in the form of a collection object.
helpviewer_keywords: ["GetTrackerDataAsCollectionObject","GetTrackerDataAsCollectionObject method [COM+]","GetTrackerDataAsCollectionObject method [COM+]","IGetAppTrackerData interface","IGetAppTrackerData interface [COM+]","GetTrackerDataAsCollectionObject method","IGetAppTrackerData.GetTrackerDataAsCollectionObject","IGetAppTrackerData::GetTrackerDataAsCollectionObject","comsvcs/IGetAppTrackerData::GetTrackerDataAsCollectionObject","cos.igetapptrackerdata_gettrackerdataascollectionobject"]
old-location: cos\igetapptrackerdata_gettrackerdataascollectionobject.htm
tech.root: cos
ms.assetid: 215523ad-5f18-4529-8b23-afbd1b738fb5
ms.date: 12/05/2018
ms.keywords: GetTrackerDataAsCollectionObject, GetTrackerDataAsCollectionObject method [COM+], GetTrackerDataAsCollectionObject method [COM+],IGetAppTrackerData interface, IGetAppTrackerData interface [COM+],GetTrackerDataAsCollectionObject method, IGetAppTrackerData.GetTrackerDataAsCollectionObject, IGetAppTrackerData::GetTrackerDataAsCollectionObject, comsvcs/IGetAppTrackerData::GetTrackerDataAsCollectionObject, cos.igetapptrackerdata_gettrackerdataascollectionobject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetAppTrackerData::GetTrackerDataAsCollectionObject
 - comsvcs/IGetAppTrackerData::GetTrackerDataAsCollectionObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetAppTrackerData.GetTrackerDataAsCollectionObject
---

# IGetAppTrackerData::GetTrackerDataAsCollectionObject


## -description

Retrieves tracking data for all COM+ applications in the form of a collection object.

## -parameters

### -param TopLevelCollection [out]

On return, the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for a collection of tracker data.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

This method is primarily intended to enable applications that subscribe to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfoevents">IComTrackingInfoEvents</a> event interface to add support for <a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a> with minimal changes to their code. The object returned by this method is identical to the object sent in calls to subscribers' <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo">IComTrackingInfoEvent::OnNewTrackingInfo</a> method, so that code for navigating and parsing this collection may be reused. 



Applications should not expect this method to return newly updated tracking data any more frequently than the server's suggested polling interval (see <a href="/windows/desktop/api/comsvcs/nf-comsvcs-igetapptrackerdata-getsuggestedpollinginterval">IGetAppTrackerData::GetSuggestedPollingInterval</a>). 



Note that the collection object returned by this method does not contain all tracking data that is available by calling the other methods. In particular, recycling details and hang monitoring configuration are not provided.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>