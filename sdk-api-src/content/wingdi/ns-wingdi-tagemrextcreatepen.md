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

# tagEMREXTCREATEPEN structure


## -description



The <b>EMREXTCREATEPEN</b> structure contains members for the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> enhanced metafile record. If the record contains a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, it is followed by the bitmap bits that form a packed device-independent bitmap (DIB).




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPen

Index to pen in handle table.


### -field offBmi

Offset to <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, if any.


### -field cbBmi

Size of <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure, if any.


### -field offBits

Offset to brush bitmap bits, if any.


### -field cbBits

Size of brush bitmap bits, if any.


### -field elp

Extended logical pen, including the <b>elpStyleEntry</b> member of the <a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/34ffa71d-e94d-425e-9f9d-21e3df4990b7">EXTLOGPEN</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

