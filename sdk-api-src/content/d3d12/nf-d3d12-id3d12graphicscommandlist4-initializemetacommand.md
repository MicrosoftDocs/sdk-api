---
UID: NF:d3d12.ID3D12GraphicsCommandList4.InitializeMetaCommand
title: ID3D12GraphicsCommandList4::InitializeMetaCommand (d3d12.h)
description: Initializes the specified meta command.
helpviewer_keywords: ["ID3D12GraphicsCommandList4 interface","InitializeMetaCommand method","ID3D12GraphicsCommandList4.InitializeMetaCommand","ID3D12GraphicsCommandList4::InitializeMetaCommand","InitializeMetaCommand","InitializeMetaCommand method","InitializeMetaCommand method","ID3D12GraphicsCommandList4 interface","d3d12/ID3D12GraphicsCommandList4::InitializeMetaCommand","direct3d12.id3d12graphicscommandlist4_initializemetacommand"]
old-location: direct3d12\id3d12graphicscommandlist4_initializemetacommand.htm
tech.root: direct3d12
ms.assetid: EC50FE25-27C7-4A5D-B4D1-57D402730AF0
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList4 interface,InitializeMetaCommand method, ID3D12GraphicsCommandList4.InitializeMetaCommand, ID3D12GraphicsCommandList4::InitializeMetaCommand, InitializeMetaCommand, InitializeMetaCommand method, InitializeMetaCommand method,ID3D12GraphicsCommandList4 interface, d3d12/ID3D12GraphicsCommandList4::InitializeMetaCommand, direct3d12.id3d12graphicscommandlist4_initializemetacommand
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
 - ID3D12GraphicsCommandList4::InitializeMetaCommand
 - d3d12/ID3D12GraphicsCommandList4::InitializeMetaCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.h
api_name:
 - ID3D12GraphicsCommandList4.InitializeMetaCommand
---

# ID3D12GraphicsCommandList4::InitializeMetaCommand


## -description

Initializes the specified meta command.

You must initialize a meta command at least once prior (on the GPU's timeline) to executing it. Initializing gives the  implementation the chance to perform any work necessary to accelerate the invocation of the meta command. You must supply the sufficient resource parameters, including the persistent cache resource.

## -parameters

### -param pMetaCommand [in]

A pointer to an <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12metacommand">ID3D12MetaCommand</a> representing the meta command to initialize.

### -param pInitializationParametersData [in, optional]

An optional pointer to a constant structure containing the values of the parameters for initializing the meta command.

### -param InitializationParametersDataSizeInBytes [in]

A <a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a> containing the size of the structure pointed to by <i>pInitializationParametersData</i>, if set, otherwise 0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>
