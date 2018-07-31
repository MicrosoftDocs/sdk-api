---
UID: NE:d3dcommon._D3D_INCLUDE_TYPE
title: "_D3D_INCLUDE_TYPE"
author: windows-sdk-content
description: Flags for indicating the location of an include file.
old-location: direct3d10\d3d10_include_type.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_include_type.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 4574facf-f245-365e-364b-b7710c758cdb, D3D10_INCLUDE_FORCE_DWORD, D3D10_INCLUDE_LOCAL, D3D10_INCLUDE_SYSTEM, D3D10_INCLUDE_TYPE, D3D10_INCLUDE_TYPE enumeration [Direct3D 10], D3D_INCLUDE_TYPE, LPD3D10_INCLUDE_TYPE, LPD3D10_INCLUDE_TYPE enumeration pointer [Direct3D 10], _D3D_INCLUDE_TYPE, d3d10shader/D3D10_INCLUDE_FORCE_DWORD, d3d10shader/D3D10_INCLUDE_LOCAL, d3d10shader/D3D10_INCLUDE_SYSTEM, d3d10shader/D3D10_INCLUDE_TYPE, d3d10shader/LPD3D10_INCLUDE_TYPE, d3dcommon/D3D10_INCLUDE_FORCE_DWORD, d3dcommon/D3D10_INCLUDE_LOCAL, d3dcommon/D3D10_INCLUDE_SYSTEM, d3dcommon/D3D10_INCLUDE_TYPE, d3dcommon/LPD3D10_INCLUDE_TYPE, direct3d10.d3d10_include_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
req.typenames: D3D_INCLUDE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
 - d3dcommon.h
api_name:
 - D3D10_INCLUDE_TYPE
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# _D3D_INCLUDE_TYPE enumeration


## -description


Flags for indicating the location of an include file.


## -enum-fields




### -field D3D_INCLUDE_LOCAL


### -field D3D_INCLUDE_SYSTEM


### -field D3D10_INCLUDE_LOCAL

The local directory.


### -field D3D10_INCLUDE_SYSTEM

The system directory.


### -field D3D_INCLUDE_FORCE_DWORD




#### - D3D10_INCLUDE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



The   <b>D3D10_INCLUDE_TYPE</b> enumeration is type defined in the  D3D10Shader.h header file as a <a href="https://msdn.microsoft.com/98f0b0dd-9ff8-4321-a9ea-2deabc9529f2">D3D_INCLUDE_TYPE</a> enumeration, which is fully defined in the  D3DCommon.h header file.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef D3D_INCLUDE_TYPE D3D10_INCLUDE_TYPE;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205156(v=VS.85).aspx">Shader Enumerations</a>
 

 

