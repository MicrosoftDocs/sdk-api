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

# AMOVERLAYFX enumeration


## -description



Specifies effects on a DirectDraw hardware overlay surface.




## -enum-fields




### -field AMOVERFX_NOFX


            Normal video (no effects).
          


### -field AMOVERFX_MIRRORLEFTRIGHT


            Mirror the overlay across the vertical axis.
          


### -field AMOVERFX_MIRRORUPDOWN


            Mirror the overlay across the horizontal axis.
          


### -field AMOVERFX_DEINTERLACE

When used in <a href="https://msdn.microsoft.com/01fdbe3d-bec7-4e66-87c5-b7e6c1044e8a">IAMOverlayFX::QueryOverlayFXCaps</a>, this flag specifies whether the hardware can support the DirectDraw 7 DDOVERFX_DEINTERLACE hint. When used with the <a href="https://msdn.microsoft.com/f8232fcf-a0d8-4155-941e-8613c09b4bbf">IAMOverlayFX::GetOverlayFX</a> or <a href="https://msdn.microsoft.com/08e44f4e-924a-4a4d-9fc5-c13b3c21c038">IAMOverlayFX::SetOverlayFX</a> methods, this flag indicates that the overlay should be deinterlaced if possible.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/6bc78464-8c9e-4016-b9aa-6589d53d45bf">IAMOverlayFX Interface</a>
 

 

