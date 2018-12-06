---
UID: NE:d2d1.D2D1_FIGURE_BEGIN
title: D2D1_FIGURE_BEGIN
author: windows-sdk-content
description: Indicates whether a specific ID2D1SimplifiedGeometrySink figure is filled or hollow.
old-location: direct2d\D2D1_FIGURE_BEGIN.htm
tech.root: direct2d
ms.assetid: c29aa79e-b978-4318-a8e1-5a321cd66327
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_FIGURE_BEGIN, D2D1_FIGURE_BEGIN enumeration [Direct2D], D2D1_FIGURE_BEGIN_FILLED, D2D1_FIGURE_BEGIN_HOLLOW, d2d1/D2D1_FIGURE_BEGIN, d2d1/D2D1_FIGURE_BEGIN_FILLED, d2d1/D2D1_FIGURE_BEGIN_HOLLOW, direct2d.D2D1_FIGURE_BEGIN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_FIGURE_BEGIN
product: Windows
targetos: Windows
req.typenames: D2D1_FIGURE_BEGIN
req.redist: 
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
 

 

