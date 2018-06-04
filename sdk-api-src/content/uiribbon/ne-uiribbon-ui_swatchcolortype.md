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

# UI_SWATCHCOLORTYPE enumeration


## -description


Specifies the values that identify how a color swatch in a <a href="https://msdn.microsoft.com/fc4df978-9c52-43d5-8a5e-e015aa7058cd">DropDownColorPicker</a> or a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> color picker (<b>Text color</b> or <b>Text highlight</b>) is filled.
<div class="alert"><b>Note</b>  These are recommendations only. The application can associate any fill type with these values.</div><div> </div>

## -enum-fields




### -field UI_SWATCHCOLORTYPE_NOCOLOR

The swatch is transparent.


### -field UI_SWATCHCOLORTYPE_AUTOMATIC

The swatch is filled with a solid RGB color bound to <a href="http://go.microsoft.com/fwlink/p/?linkid=143871">GetSysColor(COLOR_WINDOWTEXT)</a>.


### -field UI_SWATCHCOLORTYPE_RGB

The swatch is filled with a solid RGB color.


## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>
 

 

