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

# _MFVideoArea structure


## -description



          Specifies a rectangular area within a video frame.
        


## -struct-fields




### -field OffsetX


              An <a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a> structure that contains the x-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field OffsetY


              An <a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a> structure that contains the y-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field Area


              A <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that contains the width and height of the rectangle.
          


## -see-also




<a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

