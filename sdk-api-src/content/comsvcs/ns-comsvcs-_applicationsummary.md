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

# _ApplicationSummary structure


## -description


Represents a COM+ application hosted in a particular process. It can also represent a pseudo-application entry for all Services Without Components (SWC) contexts in the process.


## -struct-fields




### -field ApplicationInstanceId

The application instance GUID that uniquely identifies the process hosting the COM+ application.


### -field PartitionId

The partition ID of the COM+ application.


### -field ApplicationId

The application ID of the COM+ application. The special value {84ac4168-6fe5-4308-a2ed-03688a023c7a} is used for the SWC pseudo-application. 


### -field Type

The type of COM+ application. For a list of values, see <a href="https://msdn.microsoft.com/121d287f-067b-4640-ac81-43904463ded4">COMPLUS_APPTYPE</a>.


### -field ApplicationName

The name of the COM+ application, or an empty string for the SWC pseudo-application. Space for this string is allocated by the method called and freed by the caller (for more information, see <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>). This member is not returned by default. To return this member, specify the GATD_INCLUDE_APPLICATION_NAME flag when you call a method that returns an <a href="https://msdn.microsoft.com/2402aca6-4992-4c6e-a6ff-b4cc50c57dde">ApplicationProcessSummary</a> structure.


### -field NumTrackedComponents

The number of distinct components from this COM+ application instantiated in the hosting process.


### -field NumComponentInstances

The number of component instances from this COM+ application in the hosting process.


## -see-also




<a href="https://msdn.microsoft.com/f2f9c03b-4f57-4087-8fef-5cdccece91d9">IGetAppTrackerData</a>
 

 

