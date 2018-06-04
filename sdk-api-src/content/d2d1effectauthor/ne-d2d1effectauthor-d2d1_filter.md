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

# D2D1_FILTER enumeration


## -description


Represents filtering modes that a transform may select to use on input textures.


## -enum-fields




### -field D2D1_FILTER_MIN_MAG_MIP_POINT

Use point sampling for minification, magnification, and mip-level sampling.


### -field D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling.


### -field D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling.


### -field D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling.


### -field D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling.


### -field D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling.


### -field D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling.


### -field D2D1_FILTER_MIN_MAG_MIP_LINEAR

Use linear interpolation for minification, magnification, and mip-level sampling.


### -field D2D1_FILTER_ANISOTROPIC

Use anisotropic interpolation for minification, magnification, and mip-level sampling.


### -field D2D1_FILTER_FORCE_DWORD




## -remarks



This enumeration has the same numeric values as <a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a>.




## -see-also




<a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a>
 

 

