---
UID: NF:d2d1_3.ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &,ID2D1ColorContext1)
title: ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &,ID2D1ColorContext1) (d2d1_3.h)
description: Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.helpviewer_keywords: ["CreateColorContextFromSimpleColorProfile","CreateColorContextFromSimpleColorProfile method [Direct2D]","CreateColorContextFromSimpleColorProfile method [Direct2D]","ID2D1DeviceContext5 interface","ID2D1DeviceContext5 interface [Direct2D]","CreateColorContextFromSimpleColorProfile method","ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile","ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &","ID2D1ColorContext1)","ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile","ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &","ID2D1ColorContext1)","d2d1_3/ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile","direct2d.id2d1devicecontext5_createcolorcontextfromsimplecolorprofile_2"]
old-location: direct2d\id2d1devicecontext5_createcolorcontextfromsimplecolorprofile_2.htm
tech.root: Direct2D
ms.assetid: 6c7b1b74-3ca8-8ee9-6ff3-fba95ddc4b32
ms.date: 12/05/2018
ms.keywords: CreateColorContextFromSimpleColorProfile, CreateColorContextFromSimpleColorProfile method [Direct2D], CreateColorContextFromSimpleColorProfile method [Direct2D],ID2D1DeviceContext5 interface, ID2D1DeviceContext5 interface [Direct2D],CreateColorContextFromSimpleColorProfile method, ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile, ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &,ID2D1ColorContext1), ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile, ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &,ID2D1ColorContext1), d2d1_3/ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile, direct2d.id2d1devicecontext5_createcolorcontextfromsimplecolorprofile_2
f1_keywords:
- d2d1_3/ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile
dev_langs:
- c++
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
- ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE &,ID2D1ColorContext1)


## -description


Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.


## -parameters




### -param simpleProfile [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile">D2D1_SIMPLE_COLOR_PROFILE</a></b>

The simple color profile to create the color context from.


### -param colorContext [out]

Type: <b>ID2D1ColorContext1**</b>

The created color context.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext5">ID2D1DeviceContext5</a>
 

 

