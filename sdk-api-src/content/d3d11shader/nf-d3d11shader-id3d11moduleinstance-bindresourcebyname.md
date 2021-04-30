---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindResourceByName
title: ID3D11ModuleInstance::BindResourceByName (d3d11shader.h)
description: Rebinds a texture or buffer by name to destination slots.
helpviewer_keywords: ["BindResourceByName","BindResourceByName method [Direct3D 11]","BindResourceByName method [Direct3D 11]","ID3D11ModuleInstance interface","ID3D11ModuleInstance interface [Direct3D 11]","BindResourceByName method","ID3D11ModuleInstance.BindResourceByName","ID3D11ModuleInstance::BindResourceByName","d3d11shader/ID3D11ModuleInstance::BindResourceByName","direct3d11.id3d11moduleinstance_bindresourcebyname"]
old-location: direct3d11\id3d11moduleinstance_bindresourcebyname.htm
tech.root: direct3d11
ms.assetid: 313A4AE8-8B3A-40B9-85C4-86A43F4F37D5
ms.date: 12/05/2018
ms.keywords: BindResourceByName, BindResourceByName method [Direct3D 11], BindResourceByName method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindResourceByName method, ID3D11ModuleInstance.BindResourceByName, ID3D11ModuleInstance::BindResourceByName, d3d11shader/ID3D11ModuleInstance::BindResourceByName, direct3d11.id3d11moduleinstance_bindresourcebyname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ModuleInstance::BindResourceByName
 - d3d11shader/ID3D11ModuleInstance::BindResourceByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ModuleInstance.BindResourceByName
---

# ID3D11ModuleInstance::BindResourceByName


## -description

Rebinds a texture or buffer by name to destination slots.

## -parameters

### -param pName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the texture or buffer for rebinding.

### -param uDstSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The first destination slot number for rebinding.

### -param uCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of slots for rebinding.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns:

<ul>
<li><b>S_OK</b> for a valid rebinding</li>
<li><b>S_FALSE</b> for rebinding a nonexistent slot; that is, for which the shader reflection doesn’t have any data</li>
<li><b>E_FAIL</b> for an invalid rebinding, for example, the rebinding is out-of-bounds</li>
<li>Possibly one of the other <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance">ID3D11ModuleInstance</a>