---
UID: NF:d3d9helper.IDirect3DDevice9.EvictManagedResources
title: IDirect3DDevice9::EvictManagedResources
author: windows-sdk-content
description: Evicts all managed resources, including both Direct3D and driver-managed resources.
old-location: direct3d9\idirect3ddevice9__evictmanagedresources.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__evictmanagedresources.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EvictManagedResources, EvictManagedResources method [Direct3D 9], EvictManagedResources method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EvictManagedResources method, IDirect3DDevice9.EvictManagedResources, IDirect3DDevice9::EvictManagedResources, d3d9helper/IDirect3DDevice9::EvictManagedResources, direct3d9.idirect3ddevice9__evictmanagedresources, ec2856fb-c12d-5e50-485d-460fa48f8758
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
 - IDirect3DDevice9.EvictManagedResources
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
- IDirect3DDevice9.EvictManagedResources
: 
---

# IDirect3DDevice9::EvictManagedResources


## -description


Evicts all managed resources, including both Direct3D and driver-managed resources.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_OUTOFVIDEOMEMORY, D3DERR_COMMAND_UNPARSED.




## -remarks



This function causes only the D3DPOOL_DEFAULT copy of resources to be evicted. The resource copy in system memory is retained. See <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

