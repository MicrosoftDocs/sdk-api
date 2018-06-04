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

# __MIDL___MIDL_itf_vmr9_0000_0000_0002 enumeration


## -description



The <code>VMR9PresentationFlags</code> enumeration type contains flags that describe the status of a video sample. These flags are used in the <a href="https://msdn.microsoft.com/7e5cf0e9-1cb9-494a-9370-550328dcd85c">VMR9PresentationInfo</a> structure.




## -enum-fields




### -field VMR9Sample_SyncPoint

Indicates that the sample is a sync point.


### -field VMR9Sample_Preroll

Indicates that the sample is part of the preroll.


### -field VMR9Sample_Discontinuity

Indicates that the sample is a discontinuity.


### -field VMR9Sample_TimeValid

Indicates that the time stamp on the sample is valid.


### -field VMR9Sample_SrcDstRectsValid




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

