---
UID: NF:d3d12.ID3D12Device.CreateCommandSignature
title: ID3D12Device::CreateCommandSignature (d3d12.h)
description: This method creates a command signature.
helpviewer_keywords: ["CreateCommandSignature","CreateCommandSignature method","CreateCommandSignature method","ID3D12Device interface","ID3D12Device interface","CreateCommandSignature method","ID3D12Device.CreateCommandSignature","ID3D12Device::CreateCommandSignature","d3d12/ID3D12Device::CreateCommandSignature","direct3d12.id3d12device_createcommandsignature"]
old-location: direct3d12\id3d12device_createcommandsignature.htm
tech.root: direct3d12
ms.assetid: 5A44F907-C6E0-4548-A227-84F0CF2EE837
ms.date: 12/05/2018
ms.keywords: CreateCommandSignature, CreateCommandSignature method, CreateCommandSignature method,ID3D12Device interface, ID3D12Device interface,CreateCommandSignature method, ID3D12Device.CreateCommandSignature, ID3D12Device::CreateCommandSignature, d3d12/ID3D12Device::CreateCommandSignature, direct3d12.id3d12device_createcommandsignature
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateCommandSignature
 - d3d12/ID3D12Device::CreateCommandSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateCommandSignature
---

# ID3D12Device::CreateCommandSignature


## -description

This method creates a command signature.

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc">D3D12_COMMAND_SIGNATURE_DESC</a>*</b>

Describes the command signature to be created with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc">D3D12_COMMAND_SIGNATURE_DESC</a> structure.

### -param pRootSignature [in, optional]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a>*</b>

Specifies the  <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a> that the command signature applies to.
          

The root signature is required if any of the commands in the signature will update bindings on the pipeline. If the only command present is a draw or dispatch, the root signature parameter can be set to NULL.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command signature interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandsignature">ID3D12CommandSignature</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command signature can be obtained by using the __uuidof() macro.
            For example, __uuidof(<b>ID3D12CommandSignature</b>) will get the <b>GUID</b> of the interface to a command signature.

### -param ppvCommandSignature [out, optional]

Type: <b>void**</b>

Specifies a pointer, that on successful completion of the method will point to the created command signature (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandsignature">ID3D12CommandSignature</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>