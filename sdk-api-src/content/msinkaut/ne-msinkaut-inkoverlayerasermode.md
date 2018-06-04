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

# InkOverlayEraserMode enumeration


## -description



Specifies the way in which ink is erased from the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object and the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

This mode is used when the <a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode</a> is set to Delete.




## -enum-fields




### -field IOERM_StrokeErase

 Ink is erased by stroke.

This is the default value.


### -field IOERM_PointErase

Ink is erased by point.


## -see-also




<a href="https://msdn.microsoft.com/f6471163-8209-4dd0-887c-0edd54ebb50e">EraserMode Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/8a880a9a-acd4-4cb1-aea7-4d834ecd9490">EraserWidth Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode Enumeration</a>
 

 

