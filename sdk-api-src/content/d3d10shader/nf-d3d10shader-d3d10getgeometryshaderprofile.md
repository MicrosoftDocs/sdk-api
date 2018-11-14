---
UID: NF:d3d10shader.D3D10GetGeometryShaderProfile
title: D3D10GetGeometryShaderProfile function
author: windows-sdk-content
description: Get the geometry shader profile best suited to a given device.
old-location: direct3d10\d3d10getgeometryshaderprofile.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getgeometryshaderprofile.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10GetGeometryShaderProfile, D3D10GetGeometryShaderProfile function [Direct3D 10], ba175c86-099a-e747-2120-b83c9b421a82, d3d10shader/D3D10GetGeometryShaderProfile, direct3d10.d3d10getgeometryshaderprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3d10shader.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10GetGeometryShaderProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- D3D10GetGeometryShaderProfile
: 
---

# D3D10GetGeometryShaderProfile function


## -description


Get the geometry <a href="https://msdn.microsoft.com/en-us/library/Bb509626(v=VS.85).aspx">shader profile</a> best suited to a given device.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>*</b>

Pointer to the device (see <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The shader profile.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205157(v=VS.85).aspx">Shader Functions</a>
 

 

