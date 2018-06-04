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

# tagSources structure


## -description


The Sources structure contains a Video Present Network (VidPN) topology. 


## -struct-fields




### -field sourceId

The source identifier for the video present source in the VidPN topology. 


### -field numTargets

The number of video present targets in the array that the <b>aTargets</b> member specifies, which is the number of video present targets in the VidPN topology. 


### -field aTargets

An array of identifiers for the video present targets in the VidPN topology. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538207">Adapter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568176">IViewHelper::SetConfiguration</a>
 

 

