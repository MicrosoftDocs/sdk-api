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

# tagEMRSETPALETTEENTRIES structure


## -description



The <b>EMRSETPALETTEENTRIES</b> structure contains members for the <a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Palette handle index.


### -field iStart

Index of first entry to set.


### -field cEntries

Number of entries.


### -field aPalEntries

Array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures. Note that <b>peFlags</b> members in the structures do not contain any flags.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>



<a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a>
 

 

