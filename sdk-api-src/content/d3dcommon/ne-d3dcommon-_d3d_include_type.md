---
UID: NE:d3dcommon._D3D_INCLUDE_TYPE
title: "_D3D_INCLUDE_TYPE"
author: windows-sdk-content
description: Values that indicate the location of a shader #include file.
old-location: direct3d11\d3d_include_type.htm
tech.root: direct3d11
ms.assetid: 98f0b0dd-9ff8-4321-a9ea-2deabc9529f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_INCLUDE_LOCAL, D3D10_INCLUDE_SYSTEM, D3D_INCLUDE_FORCE_DWORD, D3D_INCLUDE_LOCAL, D3D_INCLUDE_SYSTEM, D3D_INCLUDE_TYPE, D3D_INCLUDE_TYPE enumeration [Direct3D 11], _D3D_INCLUDE_TYPE, d3dcommon/D3D10_INCLUDE_LOCAL, d3dcommon/D3D10_INCLUDE_SYSTEM, d3dcommon/D3D_INCLUDE_FORCE_DWORD, d3dcommon/D3D_INCLUDE_LOCAL, d3dcommon/D3D_INCLUDE_SYSTEM, d3dcommon/D3D_INCLUDE_TYPE, direct3d11.d3d_include_type
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_INCLUDE_TYPE
product: Windows
targetos: Windows
req.typenames: D3D_INCLUDE_TYPE
req.redist: 
---

# _D3D_INCLUDE_TYPE enumeration


## -description


Values that indicate the location of a shader #include file. 


## -enum-fields




### -field D3D_INCLUDE_LOCAL

The local directory.


### -field D3D_INCLUDE_SYSTEM

The system directory.


### -field D3D10_INCLUDE_LOCAL

The local directory.


### -field D3D10_INCLUDE_SYSTEM

The system directory.


### -field D3D_INCLUDE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. 

Do not use this value.


## -remarks



You pass a <b>D3D_INCLUDE_TYPE</b>-typed value to the  <i>IncludeType</i> parameter in a call to the  <a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a> method to indicate the location of the #include file.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>



<a href="https://msdn.microsoft.com/98f0b0dd-9ff8-4321-a9ea-2deabc9529f2">D3D_INCLUDE_TYPE</a>



<a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a>
 

 

