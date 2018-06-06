---
UID: NS:comsvcs._ApplicationSummary
title: "_ApplicationSummary"
author: windows-sdk-content
description: Represents a COM+ application hosted in a particular process. It can also represent a pseudo-application entry for all Services Without Components (SWC) contexts in the process.
old-location: cos\applicationsummary.htm
old-project: cossdk
ms.assetid: 3291eede-5318-4d97-a969-ce54381f30af
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ApplicationSummary, ApplicationSummary structure [COM+], _ApplicationSummary, comsvcs/ApplicationSummary, cos.applicationsummary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: ApplicationSummary
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ApplicationSummary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

