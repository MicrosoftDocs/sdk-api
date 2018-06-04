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

# SHCreateShellPalette function


## -description


Creates a halftone palette for the specified device context.


## -parameters




### -param hdc [in, optional]

Type: <b>HDC</b>

The device context.


## -returns



Type: <b>HPALETTE</b>

Returns the palette if successful; otherwise 0.




## -remarks



This function behaves the same as <a href="https://msdn.microsoft.com/ba9dfa0c-98df-4922-acba-d00e9b4b0fb0">CreateHalftonePalette</a>. The palette that is returned depends on the device context in the following way:

				

<ul>
<li>If <i>hdc</i> is set to <b>NULL</b>, a full palette is returned.</li>
<li>If the device context is indexed, a full palette is returned.</li>
<li>If the device context is not indexed, a default palette (VGA colors) is returned.</li>
</ul>


