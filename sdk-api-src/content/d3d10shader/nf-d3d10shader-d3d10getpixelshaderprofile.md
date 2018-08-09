---
UID: NF:d3d10shader.D3D10GetPixelShaderProfile
title: D3D10GetPixelShaderProfile function
author: windows-sdk-content
description: Get the pixel shader profile best suited to a given device.
old-location: direct3d10\d3d10getpixelshaderprofile.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getpixelshaderprofile.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 8d581e0e-4553-6a9c-455b-9ef399e0d29f, D3D10GetPixelShaderProfile, D3D10GetPixelShaderProfile function [Direct3D 10], d3d10shader/D3D10GetPixelShaderProfile, direct3d10.d3d10getpixelshaderprofile
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D10GetPixelShaderProfile
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10GetPixelShaderProfile function


## -description


Get the pixel <a href="https://msdn.microsoft.com/en-us/library/Bb509626(v=VS.85).aspx">shader profile</a> best suited to a given device.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>*</b>

Pointer to the device (see <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The shader profile.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205157(v=VS.85).aspx">Shader Functions</a>
 

 

