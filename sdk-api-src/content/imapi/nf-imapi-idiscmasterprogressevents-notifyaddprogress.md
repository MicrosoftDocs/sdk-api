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

# IDiscMasterProgressEvents::NotifyAddProgress


## -description


Notifies an application of its progress in response to calls to 
<a href="https://msdn.microsoft.com/d9bd4f3c-4ff5-4f6e-9520-27fef3736636">IRedbookDiscMaster::AddAudioTrackBlocks</a> or 
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">IJolietDiscMaster::AddData</a>. Notifications are sent for the first and last steps, and at points in between.


## -parameters




### -param nCompletedSteps [in]

Number of arbitrary steps that have been completed in adding audio or data to a staged image.


### -param nTotalSteps [in]

Total number of arbitrary steps that must be taken to add a full set of audio or data to the staged image.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 

