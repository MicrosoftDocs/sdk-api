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

# DWRITE_OUTLINE_THRESHOLD enumeration


## -description


The <b>DWRITE_OUTLINE_THRESHOLD</b> enumeration contains values that specify the policy used by the <a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">IDWriteFontFace1::GetRecommendedRenderingMode</a> method to determine whether to render glyphs in outline mode.


## -enum-fields




### -field DWRITE_OUTLINE_THRESHOLD_ANTIALIASED

Graphics system renders anti-aliased outlines.


### -field DWRITE_OUTLINE_THRESHOLD_ALIASED

Graphics system renders aliased outlines.


## -remarks



Glyphs are rendered in outline mode by default at large sizes for performance reasons, but how large (that is, the outline threshold) depends on the quality of outline rendering. If the graphics system renders anti-aliased outlines, a relatively low threshold is used. But if the graphics system renders aliased outlines, a much higher threshold is used.




## -see-also




<a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">IDWriteFontFace1::GetRecommendedRenderingMode</a>
 

 

