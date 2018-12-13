---
UID: NS:d3d11.D3D11_FEATURE_DATA_DOUBLES
title: D3D11_FEATURE_DATA_DOUBLES
author: windows-sdk-content
description: Describes double data type support in the current graphics driver.
old-location: direct3d11\d3d11_feature_data_doubles.htm
tech.root: direct3d11
ms.assetid: 3cd4006b-25bd-46b8-9fa7-6b7d7eb82a75
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_FEATURE_DATA_DOUBLES, D3D11_FEATURE_DATA_DOUBLES structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_DOUBLES, dde276ab-cd61-a449-9965-674c9221da9c, direct3d11.d3d11_feature_data_doubles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_DOUBLES
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_DOUBLES
req.redist: 
---

# D3D11_FEATURE_DATA_DOUBLES structure


## -description


Describes double data type support in the current graphics driver.


## -struct-fields




### -field DoublePrecisionFloatShaderOps

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether <a href="https://msdn.microsoft.com/bf24d27f-2720-4268-bc74-fc46afedb9aa">double</a> types are allowed. If <b>TRUE</b>, <a href="https://msdn.microsoft.com/bf24d27f-2720-4268-bc74-fc46afedb9aa">double</a> types are allowed; otherwise <b>FALSE</b>. The runtime must set <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b> in order for you to use any <a href="https://msdn.microsoft.com/09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9">HLSL</a> shader that is compiled with a <a href="https://msdn.microsoft.com/bf24d27f-2720-4268-bc74-fc46afedb9aa">double</a> type.


## -remarks



If the runtime sets <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b>, the hardware and driver support the following <a href="https://msdn.microsoft.com/ec646940-8901-45c5-a44c-434c8acae2aa">Shader Model 5</a> instructions:

<ul>
<li>
<a href="https://msdn.microsoft.com/416F1103-E27B-4AFC-9ED1-492FF8A93492">dadd</a>
</li>
<li>
<a href="https://msdn.microsoft.com/34ED8B34-2592-4BBB-BCF0-F2222E4D51D9">dmax</a>
</li>
<li>
<a href="https://msdn.microsoft.com/77331B4D-C4B5-49B2-BB6A-77BD5050B575">dmin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53AE27BE-2F4B-4C55-B496-D7122C00DC52">dmul</a>
</li>
<li>
<a href="https://msdn.microsoft.com/99806989-D3A0-43F4-832A-5F1BD9C59A11">deq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2E769077-E861-4EFA-817F-7D1AE998746C">dge</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB">dlt</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7C69A86D-0820-4640-AF5A-2993EC77D2AA">dne</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05DBB9E2-10EC-4324-BB8F-1A9E315DE90C">dmov</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E376FE08-E251-4BE5-9F15-99B3B67A29C8">dmovc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1D2EF05C-06EF-44F0-AA0F-22D3057FF43E">dtof</a>
</li>
<li>
<a href="https://msdn.microsoft.com/95297556-41ED-4ED0-8F9A-16B7A440AF25">ftod</a>
</li>
</ul>
<div class="alert"><b>Note</b>  If <b>DoublePrecisionFloatShaderOps</b> is <b>TRUE</b>, the hardware and driver do not necessarily support double-precision division.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

