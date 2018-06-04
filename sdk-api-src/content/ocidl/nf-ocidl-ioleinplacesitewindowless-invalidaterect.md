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

# IOleInPlaceSiteWindowless::InvalidateRect


## -description


Enables an object to invalidate a specified rectangle of its in-place image on the screen.


## -parameters




### -param pRect [in]

The rectangle to be invalidated, in client coordinates of the containing window. If this parameter is <b>NULL</b>, the object's full extent is invalidated.


### -param fErase [in]

Specifies whether the background within the update region is to be erased when the region is updated. If this parameter is <b>TRUE</b>, the background is erased. If this parameter is <b>FALSE</b>, the background remains unchanged.


## -returns



This method returns S_OK on success.




## -remarks



An object is only allowed to invalidate pixels contained in its own site rectangle. Any attempt to invalidate an area outside of that rectangle should result in a no-op.




## -see-also




<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>
 

 

