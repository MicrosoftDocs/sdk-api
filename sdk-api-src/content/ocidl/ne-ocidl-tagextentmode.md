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

# tagExtentMode enumeration


## -description


Indicates whether the sizing mode is content or integral sizing.


## -enum-fields




### -field DVEXTENT_CONTENT


Indicates that the container will ask the object how big it wants to be to exactly fit its content, for example, in snap-to-size operations.


### -field DVEXTENT_INTEGRAL

Indicates that the container will provide a proposed size to the object for its use in resizing.


## -see-also




<a href="https://msdn.microsoft.com/bd603de2-39db-43a1-a391-01dcfedc073f">DVEXTENTINFO</a>



<a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>
 

 

