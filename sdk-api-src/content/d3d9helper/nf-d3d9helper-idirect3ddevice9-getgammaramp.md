---
UID: NF:d3d9helper.IDirect3DDevice9.GetGammaRamp
title: IDirect3DDevice9::GetGammaRamp
author: windows-sdk-content
description: Retrieves the gamma correction ramp for the swap chain.
old-location: direct3d9\idirect3ddevice9__getgammaramp.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getgammaramp.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetGammaRamp, GetGammaRamp method [Direct3D 9], GetGammaRamp method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetGammaRamp method, IDirect3DDevice9.GetGammaRamp, IDirect3DDevice9::GetGammaRamp, b52b118d-254d-ca5b-efc0-a7e22cf186ef, d3d9helper/IDirect3DDevice9::GetGammaRamp, direct3d9.idirect3ddevice9__getgammaramp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetGammaRamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DDevice9.GetGammaRamp
: 
---

# IDirect3DDevice9::GetGammaRamp


## -description


Retrieves the gamma correction ramp for the swap chain.


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer specifying the swap chain.


### -param pRamp [in, out]

Type: <b><a href="https://msdn.microsoft.com/c596f47a-6c09-4b97-ab2f-b1da3d851aa4">D3DGAMMARAMP</a>*</b>

Pointer to an application-supplied <a href="https://msdn.microsoft.com/c596f47a-6c09-4b97-ab2f-b1da3d851aa4">D3DGAMMARAMP</a> structure to fill with the gamma correction ramp. 


## -returns



None.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/ad44b71a-f391-49bb-963d-705f6dd9325c">IDirect3DDevice9::SetGammaRamp</a>



<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

