---
UID: NF:d3d12.ID3D12PipelineState.GetCachedBlob
title: ID3D12PipelineState::GetCachedBlob
author: windows-sdk-content
description: Gets the cached blob representing the pipeline state.
old-location: direct3d12\id3d12pipelinestate_getcachedblob.htm
tech.root: direct3d12
ms.assetid: 318FCFEE-74A7-4546-989E-9AF674D2B853
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetCachedBlob, GetCachedBlob method, GetCachedBlob method,ID3D12PipelineState interface, ID3D12PipelineState interface,GetCachedBlob method, ID3D12PipelineState.GetCachedBlob, ID3D12PipelineState::GetCachedBlob, d3d12/ID3D12PipelineState::GetCachedBlob, direct3d12.id3d12pipelinestate_getcachedblob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12PipelineState.GetCachedBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12PipelineState::GetCachedBlob


## -description


Gets the cached blob representing the pipeline state.
        


## -parameters




### -param ppBlob [out]

Type: <b>ID3DBlob**</b>

After this method returns, points to the cached blob representing the pipeline state.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



Refer to the remarks for <a href="https://msdn.microsoft.com/82A0CF70-7A16-45D5-A717-0BBB35DCC5A6">D3D12_CACHED_PIPELINE_STATE</a>.




## -see-also




<a href="https://msdn.microsoft.com/DD922194-8AD2-4ADF-9AC2-46C903C56AE6">ID3D12PipelineState</a>
 

 

