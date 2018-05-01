---
UID: NF:d3d9helper.IDirect3DStateBlock9.GetDevice
title: IDirect3DStateBlock9::GetDevice method
author: windows-driver-content
description: Gets the device.
old-location: direct3d9\idirect3dstateblock9__getdevice.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dstateblock9__getdevice.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: GetDevice method [Direct3D 9], GetDevice method [Direct3D 9], IDirect3DStateBlock9 interface, GetDevice,IDirect3DStateBlock9.GetDevice, IDirect3DStateBlock9, IDirect3DStateBlock9 interface [Direct3D 9], GetDevice method, IDirect3DStateBlock9::GetDevice, d3d9helper/IDirect3DStateBlock9::GetDevice, df9ae4d3-a81f-bc7b-9ed3-3e0f1df28568, direct3d9.idirect3dstateblock9__getdevice
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DStateBlock9.GetDevice
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DStateBlock9::GetDevice method


## -description


Gets the device.


## -parameters




### -param ppDevice [in, out, retval]

Type: <b><a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>**</b>

Pointer to the IDirect3DDevice9 interface that is returned.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/bb0dfea8-14ba-4d9d-acb7-9748258e0f35">IDirect3DStateBlock9</a>
 

 

