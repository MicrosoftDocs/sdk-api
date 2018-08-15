---
UID: NF:d3d9.IDirect3D9.RegisterSoftwareDevice
title: IDirect3D9::RegisterSoftwareDevice
author: windows-sdk-content
description: Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers.
old-location: direct3d9\idirect3d9__registersoftwaredevice.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__registersoftwaredevice.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3D9 interface [Direct3D 9],RegisterSoftwareDevice method, IDirect3D9.RegisterSoftwareDevice, IDirect3D9::RegisterSoftwareDevice, RegisterSoftwareDevice, RegisterSoftwareDevice method [Direct3D 9], RegisterSoftwareDevice method [Direct3D 9],IDirect3D9 interface, d3d9helper/IDirect3D9::RegisterSoftwareDevice, direct3d9.idirect3d9__registersoftwaredevice, e610f417-a861-aa97-bbbf-2a9305b15f2d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.RegisterSoftwareDevice
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9::RegisterSoftwareDevice


## -description


Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers.


## -parameters




### -param pInitializeFunction [in]

Type: <b>void*</b>

Pointer to the initialization function for the software device to be registered. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL. The method call is invalid. For example, a method's parameter may have an invalid value: D3DERR_OUTOFVIDEOMEMORY. 




## -remarks



If the user's computer provides no special hardware acceleration for 3D operations, your application might emulate 3D hardware in software. Software rasterization devices emulate the functions of color 3D hardware in software. A software device runs more slowly than a hal. However, software devices
    
    take advantage of any special instructions supported by the CPU to increase performance. Instruction sets include the AMD 3DNow! instruction set on some AMD processors and the MMX instruction set supported by many Intel processors. Direct3D uses the 3D-Now! instruction set to accelerate transformation and lighting operations and the MMX instruction set to accelerate rasterization.

Software devices communicate with Direct3D through an interface similar to the hardware device driver interface (DDI).

Software devices are loaded by the application and registered with the <a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a> object. Direct3D uses the software device for rendering. 

The Direct3D Driver Development Kit (DDK) provides the documentation and headers for developing pluggable software devices.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a>
 

 

