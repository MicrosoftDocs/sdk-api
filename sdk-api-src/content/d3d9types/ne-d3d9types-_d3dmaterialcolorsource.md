---
UID: NE:d3d9types._D3DMATERIALCOLORSOURCE
title: "_D3DMATERIALCOLORSOURCE"
author: windows-driver-content
description: Defines the location at which a color or color component must be accessed for lighting calculations.
old-location: direct3d9\D3DMATERIALCOLORSOURCE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dmaterialcolorsource.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 2f889ba2-24f5-ba8e-45c0-6b1d5eda11f3, D3DMATERIALCOLORSOURCE, D3DMATERIALCOLORSOURCE enumeration [Direct3D 9], D3DMCS_COLOR1, D3DMCS_COLOR2, D3DMCS_FORCE_DWORD, D3DMCS_MATERIAL, LPD3DMATERIALCOLORSOURCE, LPD3DMATERIALCOLORSOURCE enumeration pointer [Direct3D 9], _D3DMATERIALCOLORSOURCE, d3d9types/D3DMATERIALCOLORSOURCE, d3d9types/D3DMCS_COLOR1, d3d9types/D3DMCS_COLOR2, d3d9types/D3DMCS_FORCE_DWORD, d3d9types/D3DMCS_MATERIAL, d3d9types/LPD3DMATERIALCOLORSOURCE, direct3d9.D3DMATERIALCOLORSOURCE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DMATERIALCOLORSOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DMATERIALCOLORSOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DMATERIALCOLORSOURCE enumeration


## -description


Defines the location at which a color or color component must be accessed for lighting calculations.


## -enum-fields




### -field D3DMCS_MATERIAL

Use the color from the current material. 


### -field D3DMCS_COLOR1

Use the diffuse vertex color. 


### -field D3DMCS_COLOR2

Use the specular vertex color. 


### -field D3DMCS_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



These flags are used to set the value of the following render states in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a> enumerated type. 

<ul>
<li>D3DRS_AMBIENTMATERIALSOURCE</li>
<li>D3DRS_DIFFUSEMATERIALSOURCE</li>
<li>D3DRS_EMISSIVEMATERIALSOURCE</li>
<li>D3DRS_SPECULARMATERIALSOURCE</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

