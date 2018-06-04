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

# D2D1_FIGURE_BEGIN enumeration


## -description


Indicates whether a specific <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a> figure is filled or hollow. 


## -enum-fields




### -field D2D1_FIGURE_BEGIN_FILLED

Indicates the figure will be filled by the FillGeometry (<a href="https://msdn.microsoft.com/04e93b19-f3a7-4196-bce0-e656d48116ef">ID2D1CommandSink::FillGeometry</a> 
          or <a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">ID2D1RenderTarget::FillGeometry</a>) method.


### -field D2D1_FIGURE_BEGIN_HOLLOW

Indicates the figure will not be filled by the FillGeometry (<a href="https://msdn.microsoft.com/04e93b19-f3a7-4196-bce0-e656d48116ef">ID2D1CommandSink::FillGeometry</a> 
          or <a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">ID2D1RenderTarget::FillGeometry</a>) method and will only consist of an outline. 
          Moreover, the bounds of a hollow figure are zero. 
          D2D1_FIGURE_BEGIN_HOLLOW should be used for stroking, or for other geometry operations.


### -field D2D1_FIGURE_BEGIN_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>



<a href="https://msdn.microsoft.com/87a932d4-1f90-4bdb-b131-0664566b0318">ID2D1SimplifiedGeometrySink::BeginFigure</a>



<a href="https://msdn.microsoft.com/38a290be-b915-4317-b9b1-0e49e40dc8ec">Path Geometries Overview</a>
 

 

