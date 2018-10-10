---
UID: NF:d2d1svg.ID2D1SvgPathData.CreatePathGeometry
title: ID2D1SvgPathData::CreatePathGeometry
author: windows-sdk-content
description: Creates a path geometry object representing the path data.
old-location: direct2d\id2d1svgpathdata_createpathgeometry.htm
tech.root: Direct2D
ms.assetid: BDF23A0F-EC4B-49AE-8822-9326DA2D885D
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreatePathGeometry, CreatePathGeometry method [Direct2D], CreatePathGeometry method [Direct2D],ID2D1SvgPathData interface, ID2D1SvgPathData interface [Direct2D],CreatePathGeometry method, ID2D1SvgPathData.CreatePathGeometry, ID2D1SvgPathData::CreatePathGeometry, d2d1svg/ID2D1SvgPathData::CreatePathGeometry, direct2d.id2d1svgpathdata_createpathgeometry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPathData.CreatePathGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPathData::CreatePathGeometry


## -description


Creates a path geometry object representing the path data.


## -parameters




### -param fillMode

Type: <b><a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE</a></b>

Fill mode for the path geometry object.


### -param pathGeometry [out]

Type: <b>ID2D1PathGeometry1**</b>

On completion, pathGeometry will contain a point to the created <a href="https://msdn.microsoft.com/21f0a4a3-3c6c-434d-8cfc-767c7654849e">ID2D1PathGeometry1</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/14879B17-0CAA-42E7-8643-7D385EABFD37">ID2D1SvgPathData</a>
 

 

