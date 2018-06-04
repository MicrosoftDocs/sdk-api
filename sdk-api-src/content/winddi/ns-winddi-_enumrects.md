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

# _ENUMRECTS structure


## -description


The ENUMRECTS structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a> function to provide information about rectangles in a clip region for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539420">CLIPOBJ_bEnum</a> function.


## -struct-fields




### -field c

Specifies the number of RECTL structures in the <b>arcl</b> array.


### -field arcl

Is an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structures that specify the coordinates of rectangles in the clip region.

