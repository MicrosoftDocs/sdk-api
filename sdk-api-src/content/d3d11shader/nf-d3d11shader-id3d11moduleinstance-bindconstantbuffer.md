---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindConstantBuffer
title: ID3D11ModuleInstance::BindConstantBuffer
author: windows-sdk-content
description: Rebinds a constant buffer from a source slot to a destination slot.
old-location: direct3d11\id3d11moduleinstance_bindconstantbuffer.htm
tech.root: direct3d11
ms.assetid: F12B8580-6D47-4C73-8281-287A0B183D7F
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: BindConstantBuffer, BindConstantBuffer method [Direct3D 11], BindConstantBuffer method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindConstantBuffer method, ID3D11ModuleInstance.BindConstantBuffer, ID3D11ModuleInstance::BindConstantBuffer, d3d11shader/ID3D11ModuleInstance::BindConstantBuffer, direct3d11.id3d11moduleinstance_bindconstantbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ModuleInstance.BindConstantBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11shader.h
: 
- ID3D11ModuleInstance.BindConstantBuffer
: 
---

# ID3D11ModuleInstance::BindConstantBuffer


## -description


Rebinds a constant buffer from a source slot to a destination slot.


## -parameters




### -param uSrcSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The source slot number for rebinding.


### -param uDstSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The destination slot number for rebinding.


### -param cbDstOffset [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The offset in bytes of the destination slot for rebinding. The offset must have 16-byte alignment.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns:

<ul>
<li><b>S_OK</b> for a valid rebinding
              </li>
<li><b>S_FALSE</b> for rebinding a nonexistent slot; that is, for which the shader reflection doesn’t have any data
              </li>
<li><b>E_FAIL</b> for an invalid rebinding, for example, the rebinding is out-of-bounds
              </li>
<li>Possibly one of the other <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a>
 

 

