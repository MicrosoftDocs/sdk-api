---
UID: NE:comsvcs.tagCSC_TrackerConfig
title: tagCSC_TrackerConfig
author: windows-sdk-content
description: Indicates whether the tracker property is added to the context in which the enclosed code runs.
old-location: cos\csc_trackerconfig.htm
old-project: cossdk
ms.assetid: 48f01634-9802-4824-b251-ccb6e71aa099
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CSC_DontUseTracker, CSC_TrackerConfig, CSC_TrackerConfig enumeration [COM+], CSC_UseTracker, _cos_CSC_TrackerConfig, comsvcs/CSC_DontUseTracker, comsvcs/CSC_TrackerConfig, comsvcs/CSC_UseTracker, cos.csc_trackerconfig, tagCSC_TrackerConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CSC_TrackerConfig
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_TrackerConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCSC_TrackerConfig enumeration


## -description


Indicates whether the tracker property is added to the context in which the enclosed code runs.


## -enum-fields




### -field CSC_DontUseTracker

The tracker property is not added to the context in which the enclosed code runs.


### -field CSC_UseTracker

The tracker property is added to the context in which the enclosed code runs.


## -remarks



This enumeration is used to configure the tracker property through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.

The tracker property is a reporting mechanism used by monitoring code to watch which code is running at a given time. It is the reporting mechanism behind the spinning balls in the Component Services administrative tool.




## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/cdeb982b-720a-4d69-9c3c-d7a5a4527991">IServiceTrackerConfig::TrackerConfig</a>
 

 

