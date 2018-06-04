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

# D2D1_BORDER_MODE enumeration


## -description



          Specifies how the <a href="https://msdn.microsoft.com/DFB7DE20-F202-4E7F-AE63-94BF817B6E30">Crop effect</a> handles the crop rectangle falling on fractional pixel coordinates.
        


## -enum-fields




### -field D2D1_BORDER_MODE_SOFT

 If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.


### -field D2D1_BORDER_MODE_HARD

If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge. 


### -field D2D1_BORDER_MODE_FORCE_DWORD



