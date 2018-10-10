---
UID: NF:d2d1_3.ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE,ID2D1ColorContext1)
title: ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE,ID2D1ColorContext1)
author: windows-sdk-content
description: Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.
old-location: direct2d\id2d1devicecontext5_createcolorcontextfromsimplecolorprofile.htm
tech.root: Direct2D
ms.assetid: 27727A6C-2DF2-432B-AFBF-CF63BD9E5B53
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreateColorContextFromSimpleColorProfile, CreateColorContextFromSimpleColorProfile method [Direct2D], CreateColorContextFromSimpleColorProfile method [Direct2D],ID2D1DeviceContext5 interface, ID2D1DeviceContext5 interface [Direct2D],CreateColorContextFromSimpleColorProfile method, ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile, ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE,ID2D1ColorContext1), ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile, ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE,ID2D1ColorContext1), d2d1_3/ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile, direct2d.id2d1devicecontext5_createcolorcontextfromsimplecolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext5.CreateColorContextFromSimpleColorProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile(const D2D1_SIMPLE_COLOR_PROFILE,ID2D1ColorContext1)


## -description


Creates a color context from a simple color profile. It is only valid to use this with the Color Management Effect in 'Best' mode.


## -parameters




### -param simpleProfile [in]

Type: <b>const <a href="https://msdn.microsoft.com/B48A7333-AC8B-4965-9D78-6FFC3B0F01A9">D2D1_SIMPLE_COLOR_PROFILE</a>*</b>

The simple color profile to create the color context from.


### -param colorContext [out]

Type: <b>ID2D1ColorContext1**</b>

The created color context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/38689191-3315-44F3-A259-DC1EB378485D">ID2D1DeviceContext5</a>
 

 

