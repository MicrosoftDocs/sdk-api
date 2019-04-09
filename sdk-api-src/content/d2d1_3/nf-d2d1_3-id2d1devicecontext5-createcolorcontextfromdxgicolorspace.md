---
UID: NF:d2d1_3.ID2D1DeviceContext5.CreateColorContextFromDxgiColorSpace
title: ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace (d2d1_3.h)
author: windows-sdk-content
description: Creates a color context from a DXGI color space type. It is only valid to use this with the Color Management Effect in 'Best' mode.
old-location: direct2d\id2d1devicecontext5_createcolorcontextfromdxgicolorspace.htm
tech.root: Direct2D
ms.assetid: A8C785A1-0C16-4C16-9217-C54F1B911095
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateColorContextFromDxgiColorSpace, CreateColorContextFromDxgiColorSpace method [Direct2D], CreateColorContextFromDxgiColorSpace method [Direct2D],ID2D1DeviceContext5 interface, ID2D1DeviceContext5 interface [Direct2D],CreateColorContextFromDxgiColorSpace method, ID2D1DeviceContext5.CreateColorContextFromDxgiColorSpace, ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace, d2d1_3/ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace, direct2d.id2d1devicecontext5_createcolorcontextfromdxgicolorspace
ms.topic: method
req.header: d2d1_3.h
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext5.CreateColorContextFromDxgiColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace


## -description


Creates a color context from a DXGI color space type. It is only valid to use this with the Color Management Effect in 'Best' mode.


## -parameters




### -param colorSpace

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The color space to create the color context from.


### -param colorContext [out]

Type: <b>ID2D1ColorContext1**</b>

The created color context.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/38689191-3315-44F3-A259-DC1EB378485D">ID2D1DeviceContext5</a>
 

 

