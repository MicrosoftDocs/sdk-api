---
UID: NF:d3d9.IDirect3DDevice9.EvictManagedResources
title: IDirect3DDevice9::EvictManagedResources
author: windows-driver-content
description: Evicts all managed resources, including both Direct3D and driver-managed resources.
old-location: direct3d9\idirect3ddevice9__evictmanagedresources.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__evictmanagedresources.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: EvictManagedResources, EvictManagedResources method [Direct3D 9], EvictManagedResources method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EvictManagedResources method, IDirect3DDevice9.EvictManagedResources, IDirect3DDevice9::EvictManagedResources, d3d9helper/IDirect3DDevice9::EvictManagedResources, direct3d9.idirect3ddevice9__evictmanagedresources, ec2856fb-c12d-5e50-485d-460fa48f8758
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9.EvictManagedResources
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::EvictManagedResources


## -description


Evicts all managed resources, including both Direct3D and driver-managed resources.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_OUTOFVIDEOMEMORY, D3DERR_COMMAND_UNPARSED.




## -remarks



This function causes only the D3DPOOL_DEFAULT copy of resources to be evicted. The resource copy in system memory is retained. See <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

