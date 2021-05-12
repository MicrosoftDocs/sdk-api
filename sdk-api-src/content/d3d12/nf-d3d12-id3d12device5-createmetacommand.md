---
UID: NF:d3d12.ID3D12Device5.CreateMetaCommand
title: ID3D12Device5::CreateMetaCommand (d3d12.h)
description: Creates an instance of the specified meta command.
helpviewer_keywords: ["CreateMetaCommand","CreateMetaCommand method","CreateMetaCommand method","ID3D12Device5 interface","ID3D12Device5 interface","CreateMetaCommand method","ID3D12Device5.CreateMetaCommand","ID3D12Device5::CreateMetaCommand","d3d12/ID3D12Device5::CreateMetaCommand","direct3d12.id3d12device5_createmetacommand"]
old-location: direct3d12\id3d12device5_createmetacommand.htm
tech.root: direct3d12
ms.assetid: 70AB644F-7406-4271-89C9-8D38FE3B4D7A
ms.date: 12/05/2018
ms.keywords: CreateMetaCommand, CreateMetaCommand method, CreateMetaCommand method,ID3D12Device5 interface, ID3D12Device5 interface,CreateMetaCommand method, ID3D12Device5.CreateMetaCommand, ID3D12Device5::CreateMetaCommand, d3d12/ID3D12Device5::CreateMetaCommand, direct3d12.id3d12device5_createmetacommand
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device5::CreateMetaCommand
 - d3d12/ID3D12Device5::CreateMetaCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device5.CreateMetaCommand
---

## -description

Creates an instance of the specified meta command.

## -parameters

### -param CommandId [in]

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the meta command that you wish to instantiate.

### -param NodeMask [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

For single-adapter operation, set this to zero. If there are multiple adapter nodes, set a bit to identify the node (one of the device's physical adapters) to which the meta command applies. Each bit in the mask corresponds to a single node. Only one bit must be set. See <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -param pCreationParametersData [in, optional]

Type: <b>const <a href="/windows/win32/WinProg/windows-data-types">void</a>*</b>

An optional pointer to a constant structure containing the values of the parameters for creating the meta command.

### -param CreationParametersDataSizeInBytes [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">SIZE_T</a></b>

A <a href="/windows/win32/WinProg/windows-data-types">SIZE_T</a> containing the size of the structure pointed to by <i>pCreationParametersData</i>, if set, otherwise 0.

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppMetaCommand</i>. This is expected to be the GUID of <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand">ID3D12MetaCommand</a>.

### -param ppMetaCommand [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the meta command. This is the address of a pointer to an <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand">ID3D12MetaCommand</a>, representing  the meta command created.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DXGI_ERROR_UNSUPPORTED</dt>
</dl>
</td>
<td width="60%">
The current hardware does not support the algorithm being requested

</td>
</tr>
</table>

## -see-also

<a href="../d3d12/nn-d3d12-id3d12device5.md">ID3D12Device5</a>

