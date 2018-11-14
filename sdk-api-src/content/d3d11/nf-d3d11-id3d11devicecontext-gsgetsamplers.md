---
UID: NF:d3d11.ID3D11DeviceContext.GSGetSamplers
title: ID3D11DeviceContext::GSGetSamplers
author: windows-sdk-content
description: Get an array of sampler state interfaces from the geometry shader pipeline stage.
old-location: direct3d11\id3d11devicecontext_gsgetsamplers.htm
tech.root: direct3d11
ms.assetid: 7f3d4eb4-30e6-42bf-98e2-08a9abcb3e94
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GSGetSamplers, GSGetSamplers method [Direct3D 11], GSGetSamplers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSGetSamplers method, ID3D11DeviceContext.GSGetSamplers, ID3D11DeviceContext::GSGetSamplers, d3d11/ID3D11DeviceContext::GSGetSamplers, direct3d11.id3d11devicecontext_gsgetsamplers, ebfcd5c2-8164-421f-c5f3-466bdd187a65
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GSGetSamplers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.GSGetSamplers
: 
---

# ID3D11DeviceContext::GSGetSamplers


## -description


Get an array of sampler state interfaces from the geometry shader pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index into a zero-based array to begin getting samplers from (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - 1).


### -param NumSamplers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of samplers to get from a device context. Each pipeline stage has a total of 16 sampler slots available (ranges from 0 to D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT - StartSlot).


### -param ppSamplers [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476588(v=VS.85).aspx">ID3D11SamplerState</a>**</b>

Pointer to an array of sampler-state interfaces (see <a href="https://msdn.microsoft.com/en-us/library/Ff476588(v=VS.85).aspx">ID3D11SamplerState</a>).


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

