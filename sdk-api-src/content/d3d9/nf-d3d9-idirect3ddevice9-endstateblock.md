---
UID: NF:d3d9.IDirect3DDevice9.EndStateBlock
title: IDirect3DDevice9::EndStateBlock
author: windows-sdk-content
description: Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.
old-location: direct3d9\idirect3ddevice9__endstateblock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__endstateblock.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 1893d4cf-9e96-8cbc-4c69-17f309bf0986, EndStateBlock, EndStateBlock method [Direct3D 9], EndStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EndStateBlock method, IDirect3DDevice9.EndStateBlock, IDirect3DDevice9::EndStateBlock, d3d9helper/IDirect3DDevice9::EndStateBlock, direct3d9.idirect3ddevice9__endstateblock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
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
 - IDirect3DDevice9.EndStateBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::EndStateBlock


## -description


Signals Direct3D to stop recording a device-state block and retrieve a pointer to the state block interface.


## -parameters




### -param ppSB [in, retval]

Type: <b><a href="https://msdn.microsoft.com/bb0dfea8-14ba-4d9d-acb7-9748258e0f35">IDirect3DStateBlock9</a>**</b>

Pointer to a state block interface. See <a href="https://msdn.microsoft.com/bb0dfea8-14ba-4d9d-acb7-9748258e0f35">IDirect3DStateBlock9</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/ee197fbc-d13b-42c2-a293-72306a0d05ce">IDirect3DDevice9::BeginStateBlock</a>



<a href="https://msdn.microsoft.com/36951221-ab14-45bc-bfb3-4294e3d20fb0">IDirect3DDevice9::CreateStateBlock</a>
 

 

