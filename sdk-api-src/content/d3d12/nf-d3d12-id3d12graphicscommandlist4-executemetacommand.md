---
UID: NF:d3d12.ID3D12GraphicsCommandList4.ExecuteMetaCommand
title: ID3D12GraphicsCommandList4::ExecuteMetaCommand (d3d12.h)
description: Records the execution (or invocation) of the specified meta command into a graphics command list.
helpviewer_keywords: ["ExecuteMetaCommand","ExecuteMetaCommand method","ExecuteMetaCommand method","ID3D12GraphicsCommandList4 interface","ID3D12GraphicsCommandList4 interface","ExecuteMetaCommand method","ID3D12GraphicsCommandList4.ExecuteMetaCommand","ID3D12GraphicsCommandList4::ExecuteMetaCommand","d3d12/ID3D12GraphicsCommandList4::ExecuteMetaCommand","direct3d12.id3d12graphicscommandlist4_executemetacommand"]
old-location: direct3d12\id3d12graphicscommandlist4_executemetacommand.htm
tech.root: direct3d12
ms.assetid: 208D3152-C0CA-40C4-A990-8815C69E73FB
ms.date: 12/05/2018
ms.keywords: ExecuteMetaCommand, ExecuteMetaCommand method, ExecuteMetaCommand method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,ExecuteMetaCommand method, ID3D12GraphicsCommandList4.ExecuteMetaCommand, ID3D12GraphicsCommandList4::ExecuteMetaCommand, d3d12/ID3D12GraphicsCommandList4::ExecuteMetaCommand, direct3d12.id3d12graphicscommandlist4_executemetacommand
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
 - ID3D12GraphicsCommandList4::ExecuteMetaCommand
 - d3d12/ID3D12GraphicsCommandList4::ExecuteMetaCommand
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
 - ID3D12GraphicsCommandList4.ExecuteMetaCommand
---

# ID3D12GraphicsCommandList4::ExecuteMetaCommand


## -description

Records the execution (or invocation) of the specified meta command into a graphics command list.

Call <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand">ID3D12GraphicsCommandList4::InitializeMetaCommand</a> before executing a meta command. During invocation, you can specify overrides for values of any of the runtime parameters. You can execute multiple meta commands on the same graphics command list. And you can execute the same meta command multiple times on the same command list.

With a PIX capture taken with the use of meta commands, you can play that back on the same hardware configuration. But, by design, it's not portable to other GPUs.

## -parameters

### -param pMetaCommand [in]

A pointer to an <b>ID3D12MetaCommand</b> representing the meta command to initialize.

### -param pExecutionParametersData [in, optional]

An optional pointer to a constant structure containing the values of the parameters for executing the meta command.

### -param ExecutionParametersDataSizeInBytes [in]

A <a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a> containing the size of the structure pointed to by <i>pExecutionParametersData</i>, if set, otherwise 0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Your application is responsible for setting up the resources supplied to a meta command in the state required according to the meta command specification. The meta command definition specification defines the expected resource state for each parameter.
Your application is responsible for inserting unordered access view (UAV) barriers for input resources before the meta command's algorithm can consume them. You're also responsible for inserting the UAV barrier for the output resources when you intend to read them back.

During an algorithm invocation, the driver may insert as many UAV barriers to output resources as are needed to synchronize the output resource usage in the algorithm implementation. From your application's point of view, you should assume that all out and in/out resources are written to by the meta command, including scratch memory.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>
