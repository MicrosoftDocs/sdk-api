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

# ASF_SELECTION_STATUS enumeration


## -description



Defines the selection options for an ASF stream.




## -enum-fields




### -field ASF_STATUS_NOTSELECTED

No samples from the stream are delivered.


### -field ASF_STATUS_CLEANPOINTSONLY

Only samples from the stream that are clean points are delivered.


### -field ASF_STATUS_ALLDATAUNITS

All samples from the stream are delivered.


## -see-also




<a href="https://msdn.microsoft.com/82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c">IMFASFStreamSelector::GetBandwidthStep</a>



<a href="https://msdn.microsoft.com/64413669-bcb9-47fa-9362-b3f6831e55fb">IMFASFStreamSelector::GetOutputOverride</a>



<a href="https://msdn.microsoft.com/c8affecd-107f-4701-88df-200db06ad49e">IMFASFStreamSelector::SetOutputOverride</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

