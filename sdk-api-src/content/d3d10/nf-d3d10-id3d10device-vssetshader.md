---
UID: NF:d3d10.ID3D10Device.VSSetShader
title: ID3D10Device::VSSetShader
author: windows-sdk-content
description: Set a vertex shader to the device.
old-location: direct3d10\id3d10device_vssetshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vssetshader.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 8aebab54-e44a-a11b-1d07-449a345b9922, ID3D10Device interface [Direct3D 10],VSSetShader method, ID3D10Device.VSSetShader, ID3D10Device::VSSetShader, VSSetShader, VSSetShader method [Direct3D 10], VSSetShader method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSSetShader, direct3d10.id3d10device_vssetshader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.VSSetShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::VSSetShader


## -description


Set a vertex shader to the device.


## -parameters




### -param pVertexShader [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader</a>*</b>

Pointer to a vertex shader (see <a href="https://msdn.microsoft.com/library/Bb173875(v=VS.85).aspx">ID3D10VertexShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.


## -returns



Returns nothing.




## -remarks



The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

