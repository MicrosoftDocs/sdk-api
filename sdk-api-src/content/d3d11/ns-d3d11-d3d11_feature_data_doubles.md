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

Specifies whether <a href="https://msdn.microsoft.com/en-us/library/Bb509646(v=VS.85).aspx">double</a> types are allowed. If <b>TRUE</b>, <a href="https://msdn.microsoft.com/en-us/library/Bb509646(v=VS.85).aspx">double</a> types are allowed; otherwise <b>FALSE</b>. The runtime must set <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b> in order for you to use any <a href="https://msdn.microsoft.com/en-us/library/Bb509561(v=VS.85).aspx">HLSL</a> shader that is compiled with a <a href="https://msdn.microsoft.com/en-us/library/Bb509646(v=VS.85).aspx">double</a> type.


## -remarks



If the runtime sets <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b>, the hardware and driver support the following <a href="https://msdn.microsoft.com/en-us/library/Ff471356(v=VS.85).aspx">Shader Model 5</a> instructions:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446894(v=VS.85).aspx">dadd</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446974(v=VS.85).aspx">dmax</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446976(v=VS.85).aspx">dmin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446982(v=VS.85).aspx">dmul</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446947(v=VS.85).aspx">deq</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446954(v=VS.85).aspx">dge</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446973(v=VS.85).aspx">dlt</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446985(v=VS.85).aspx">dne</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446980(v=VS.85).aspx">dmov</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446978(v=VS.85).aspx">dmovc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446996(v=VS.85).aspx">dtof</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh447074(v=VS.85).aspx">ftod</a>
</li>
</ul>
<div class="alert"><b>Note</b>  If <b>DoublePrecisionFloatShaderOps</b> is <b>TRUE</b>, the hardware and driver do not necessarily support double-precision division.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

