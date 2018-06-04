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

# tagExtentInfo structure


## -description


Represents the sizing data used in <a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field dwExtentMode

Indicates whether the sizing mode is content or integral sizing. See the <a href="https://msdn.microsoft.com/5848c26d-d185-4ad9-8841-bb8b622364ee">DVEXTENTMODE</a> enumeration for possible values.


### -field sizelProposed

The proposed size in content sizing or the preferred size in integral sizing.


## -see-also




<a href="https://msdn.microsoft.com/5848c26d-d185-4ad9-8841-bb8b622364ee">DVEXTENTMODE</a>



<a href="https://msdn.microsoft.com/5759c482-2dea-4b94-956d-9560f72acbd5">IViewObjectEx::GetNaturalExtent</a>
 

 

