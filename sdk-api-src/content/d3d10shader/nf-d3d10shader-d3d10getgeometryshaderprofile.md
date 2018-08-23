---
UID: NF:d3d10shader.D3D10GetGeometryShaderProfile
title: D3D10GetGeometryShaderProfile function
author: windows-sdk-content
description: Get the geometry shader profile best suited to a given device.
old-location: direct3d10\d3d10getgeometryshaderprofile.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getgeometryshaderprofile.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: D3D10GetGeometryShaderProfile, D3D10GetGeometryShaderProfile function [Direct3D 10], ba175c86-099a-e747-2120-b83c9b421a82, d3d10shader/D3D10GetGeometryShaderProfile, direct3d10.d3d10getgeometryshaderprofile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10shader.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_MESSAGE
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10GetGeometryShaderProfile function


## -description


Get the geometry <a href="https://msdn.microsoft.com/6224f05e-20b1-42ea-96fb-63dd0edb720e">shader profile</a> best suited to a given device.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>*</b>

Pointer to the device (see <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The shader profile.




## -see-also




<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

