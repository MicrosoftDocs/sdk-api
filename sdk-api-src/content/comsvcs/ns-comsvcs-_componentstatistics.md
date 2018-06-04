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

# _ComponentStatistics structure


## -description


Represents statistical information about a COM+ component hosted in a particular process.


## -struct-fields




### -field NumInstances

The number of instances of the component in the hosting process.


### -field NumBoundReferences

The number of client references bound to an instance of this component.


### -field NumPooledObjects

The number of instances of the component in the hosting process's object pool.


### -field NumObjectsInCall

The number of instances of the component that are currently servicing a call.


### -field AvgResponseTimeInMs

A rolling average of the time it takes an instance of this component to service a call.


### -field NumCallsCompletedRecent

The number of calls to instances of this component that have completed (successfully or not) in a recent time period (for comparison with <b>NumCallsFailedRecent</b>).


### -field NumCallsFailedRecent

The number of calls to instances of this component that have failed in a recent time period (for comparison with <b>NumCallsCompletedRecent</b>).


### -field NumCallsCompletedTotal

The total number of calls to instances of this component that have completed (successfully or not) throughout the lifetime of the hosting process. This data is not currently available, and this member is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field NumCallsFailedTotal

The total number of calls to instances of this component that have failed throughout the lifetime of the hosting process. This data is not currently available, and this member is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved1

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved2

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved3

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


### -field Reserved4

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

