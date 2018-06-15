---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindConstantBuffer
title: ID3D11ModuleInstance::BindConstantBuffer
author: windows-sdk-content
description: Rebinds a constant buffer from a source slot to a destination slot.
old-location: direct3d11\id3d11moduleinstance_bindconstantbuffer.htm
old-project: direct3d11
ms.assetid: F12B8580-6D47-4C73-8281-287A0B183D7F
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: BindConstantBuffer, BindConstantBuffer method [Direct3D 11], BindConstantBuffer method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindConstantBuffer method, ID3D11ModuleInstance.BindConstantBuffer, ID3D11ModuleInstance::BindConstantBuffer, d3d11shader/ID3D11ModuleInstance::BindConstantBuffer, direct3d11.id3d11moduleinstance_bindconstantbuffer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_SHADER_VERSION_TYPE
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ModuleInstance::BindConstantBuffer


## -description


Rebinds a constant buffer from a source slot to a destination slot.


## -parameters




### -param uSrcSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The source slot number for rebinding.


### -param uDstSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The destination slot number for rebinding.


### -param cbDstOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset in bytes of the destination slot for rebinding. The offset must have 16-byte alignment.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns:

<ul>
<li><b>S_OK</b> for a valid rebinding
              </li>
<li><b>S_FALSE</b> for rebinding a nonexistent slot; that is, for which the shader reflection doesn’t have any data
              </li>
<li><b>E_FAIL</b> for an invalid rebinding, for example, the rebinding is out-of-bounds
              </li>
<li>
                Possibly one of the other <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a>
 

 

