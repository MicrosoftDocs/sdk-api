---
UID: NE:d2d1effects_2.D2D1_LOOKUPTABLE3D_PROP
title: D2D1_LOOKUPTABLE3D_PROP
author: windows-sdk-content
description: Identifiers for the properties of the 3D Lookup Table effect.
old-location: direct2d\d2d1_lookuptable3d_prop.htm
old-project: Direct2D
ms.assetid: A0F866CD-78FE-441E-810E-763347F84323
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_LOOKUPTABLE3D_PROP, D2D1_LOOKUPTABLE3D_PROP enumeration [Direct2D], D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE, D2D1_LOOKUPTABLE3D_PROP_LUT, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_LUT, direct2d.d2d1_lookuptable3d_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_2.h
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
tech.root: 
req.typenames: D2D1_LOOKUPTABLE3D_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_LOOKUPTABLE3D_PROP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_LOOKUPTABLE3D_PROP enumeration


## -description


Identifiers for the properties of the 3D Lookup Table effect.


## -enum-fields




### -field D2D1_LOOKUPTABLE3D_PROP_LUT

The D2D1_LOOKUPTABLE3D_PROP_LUT property is a pointer to an <a href="https://msdn.microsoft.com/778D2F30-0328-4AA2-8ECA-F443D57809D7">ID2D1LookupTable3D</a> object.  The default value is null.


### -field D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE

The D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE property is a <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE</a> value indicating the alpha mode of the input file.
          See the About Alpha Modes section of the <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a> topic for additional information.


### -field D2D1_LOOKUPTABLE3D_PROP_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/A76F6AB8-16E9-45C9-A768-5E4AA072D534">Built-in Effects</a>



<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">CreateEffect</a>
 

 

