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

# D2D1_CROP_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/DFB7DE20-F202-4E7F-AE63-94BF817B6E30">Crop effect</a>.


## -enum-fields




### -field D2D1_CROP_PROP_RECT


            The region to be cropped specified as a vector in the form (left, top, width, height). Units are in DIPs.
            

<div class="alert"><b>Note</b>  The rectangle will be truncated if it overlaps the edge boundaries of the input image.</div>
<div> </div>
Type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>


Default value is {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}


### -field D2D1_CROP_PROP_BORDER_MODE

Indicates how the effect handles the crop rectangle falling on fractional pixel coordinates.
          

Type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

Default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_CROP_PROP_FORCE_DWORD



