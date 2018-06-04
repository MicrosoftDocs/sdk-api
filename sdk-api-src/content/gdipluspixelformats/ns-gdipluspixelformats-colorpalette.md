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

# ColorPalette structure


## -description


The <b>ColorPalette</b> structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.


## -struct-fields




### -field Flags

Type: <b>UINT</b>

Combination of flags from the <a href="https://msdn.microsoft.com/60b44f93-600a-4041-bcee-ac75fa9339c9">PaletteFlags</a> enumeration. 


### -field Count

Type: <b>UINT</b>

Number of elements in the <b>Entries</b> array.


### -field Entries

Type: <b>ARGB[1]</b>

Array of ARGB colors. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/ffe250ce-0ebc-4470-846f-f45a1de5165e">Image::GetPalette</a>



<a href="https://msdn.microsoft.com/62f1c8c0-788b-41e6-91af-15019b65bc3d">Image::SetPalette</a>



<a href="https://msdn.microsoft.com/fac60d01-d07e-41e9-98a3-34c592d97a92">Types of Bitmaps</a>
 

 

