---
UID: NF:d3d12.ID3D12MetaCommand.GetRequiredParameterResourceSize
title: ID3D12MetaCommand::GetRequiredParameterResourceSize (d3d12.h)
description: Retrieves the amount of memory required for the specified runtime parameter resource for a meta command, for the specified stage.
helpviewer_keywords: ["GetRequiredParameterResourceSize","GetRequiredParameterResourceSize method","GetRequiredParameterResourceSize method","ID3D12MetaCommand interface","ID3D12MetaCommand interface","GetRequiredParameterResourceSize method","ID3D12MetaCommand.GetRequiredParameterResourceSize","ID3D12MetaCommand::GetRequiredParameterResourceSize","d3d12/ID3D12MetaCommand::GetRequiredParameterResourceSize","direct3d12.id3d12metacommand_getrequiredparameterresourcesize"]
old-location: direct3d12\id3d12metacommand_getrequiredparameterresourcesize.htm
tech.root: direct3d12
ms.assetid: DE619146-CEF7-4D8C-A4E7-D2BCE1BD1FBC
ms.date: 12/05/2018
ms.keywords: GetRequiredParameterResourceSize, GetRequiredParameterResourceSize method, GetRequiredParameterResourceSize method,ID3D12MetaCommand interface, ID3D12MetaCommand interface,GetRequiredParameterResourceSize method, ID3D12MetaCommand.GetRequiredParameterResourceSize, ID3D12MetaCommand::GetRequiredParameterResourceSize, d3d12/ID3D12MetaCommand::GetRequiredParameterResourceSize, direct3d12.id3d12metacommand_getrequiredparameterresourcesize
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
 - ID3D12MetaCommand::GetRequiredParameterResourceSize
 - d3d12/ID3D12MetaCommand::GetRequiredParameterResourceSize
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
 - ID3D12MetaCommand.GetRequiredParameterResourceSize
---

# ID3D12MetaCommand::GetRequiredParameterResourceSize


## -description

Retrieves the amount of memory required for the  specified  runtime parameter resource for a meta command, for the specified stage.

## -parameters

### -param Stage [in]

Type: <b>D3D12_META_COMMAND_PARAMETER_STAGE</b>

A <b>D3D12_META_COMMAND_PARAMETER_STAGE</b> specifying the stage to which the parameter belongs.

### -param ParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The zero-based index of the parameter within the stage.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The number of bytes required for the  specified  runtime parameter resource.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12metacommand">ID3D12MetaCommand</a>