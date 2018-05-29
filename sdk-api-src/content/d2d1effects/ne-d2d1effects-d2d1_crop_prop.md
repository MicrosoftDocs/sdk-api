---
UID: NE:d2d1effects.D2D1_CROP_PROP
title: D2D1_CROP_PROP
author: windows-sdk-content
description: Identifiers for properties of the Crop effect.
old-location: direct2d\d2d1_crop_prop.htm
old-project: Direct2D
ms.assetid: E9C00E8A-AD1E-475C-9B81-A5EB995669C6
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_CROP_PROP, D2D1_CROP_PROP enumeration [Direct2D], D2D1_CROP_PROP_BORDER_MODE, D2D1_CROP_PROP_RECT, d2d1effects/D2D1_CROP_PROP, d2d1effects/D2D1_CROP_PROP_BORDER_MODE, d2d1effects/D2D1_CROP_PROP_RECT, direct2d.d2d1_crop_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
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
req.typenames: D2D1_CROP_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1effects.h
api_name:
-	D2D1_CROP_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_CROP_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/DFB7DE20-F202-4E7F-AE63-94BF817B6E30">Crop effect</a>.


## -enum-fields




### -field D2D1_CROP_PROP_RECT


            The region to be cropped specified as a vector in the form (left, top, width, height). Units are in DIPs.
            

<div class="alert"><b>Note</b>  The rectangle will be truncated if it overlaps the edge boundaries of the input image.</div>
<div> </div>
Type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>


Default value is {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}


### -field D2D1_CROP_PROP_BORDER_MODE

Indicates how the effect handles the crop rectangle falling on fractional pixel coordinates.
          

Type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

Default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_CROP_PROP_FORCE_DWORD



