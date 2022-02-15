---
UID: NF:d3d12.ID3D12Device1.CreatePipelineLibrary
title: ID3D12Device1::CreatePipelineLibrary (d3d12.h)
description: Creates a cached pipeline library.
helpviewer_keywords: ["CreatePipelineLibrary","CreatePipelineLibrary method","CreatePipelineLibrary method","ID3D12Device1 interface","ID3D12Device1 interface","CreatePipelineLibrary method","ID3D12Device1.CreatePipelineLibrary","ID3D12Device1::CreatePipelineLibrary","d3d12/ID3D12Device1::CreatePipelineLibrary","direct3d12.id3d12device1_createpipelinelibrary"]
old-location: direct3d12\id3d12device1_createpipelinelibrary.htm
tech.root: direct3d12
ms.assetid: 572A95A6-A02F-4512-9BDE-2A8CA58A0A27
ms.date: 12/05/2018
ms.keywords: CreatePipelineLibrary, CreatePipelineLibrary method, CreatePipelineLibrary method,ID3D12Device1 interface, ID3D12Device1 interface,CreatePipelineLibrary method, ID3D12Device1.CreatePipelineLibrary, ID3D12Device1::CreatePipelineLibrary, d3d12/ID3D12Device1::CreatePipelineLibrary, direct3d12.id3d12device1_createpipelinelibrary
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device1::CreatePipelineLibrary
 - d3d12/ID3D12Device1::CreatePipelineLibrary
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
 - ID3D12Device1.CreatePipelineLibrary
---

## -description

Creates a cached pipeline library. For pipeline state objects (PSOs) that are expected to share data together, grouping them into a library before serializing them means that there's less overhead due to metadata, as well as the opportunity to avoid redundant or duplicated data being written to disk.

You can query for **ID3D12PipelineLibrary** support with <b><a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">ID3D12Device::CheckFeatureSupport</a></b>, with <b><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE_SHADER_CACHE</a></b> and <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache">D3D12_FEATURE_DATA_SHADER_CACHE</a></b>. If the *Flags* member of <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache">D3D12_FEATURE_DATA_SHADER_CACHE</a></b> contains the flag <b><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags">D3D12_SHADER_CACHE_SUPPORT_LIBRARY</a></b>, the **ID3D12PipelineLibrary** interface is supported. If not, then **DXGI_ERROR_NOT_SUPPORTED** will always be returned when this function is called.

## -parameters

### -param pLibraryBlob

Type: [in] **const void\***

If the input library blob is empty, then the initial content of the library is empty. If the input library blob is not empty, then it is validated for integrity, parsed, and the pointer is stored. The pointer provided as input to this method must remain valid for the lifetime of the object returned. For efficiency reasons, the data is not copied.

### -param BlobLength

Type: **[SIZE_T](/windows/win32/winprog/windows-data-types)**

Specifies the length of *pLibraryBlob* in bytes.

### -param riid

Type: **REFIID**

Specifies a unique REFIID for the [ID3D12PipelineLibrary](./nn-d3d12-id3d12pipelinelibrary.md) object. Typically set this and the following parameter with the macro `IID_PPV_ARGS(&Library)`, where **Library** is the name of the object.

### -param ppPipelineLibrary

Type: [out] **void\*\***

Returns a pointer to the created library.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10), including **E_INVALIDARG** if the blob is corrupted or unrecognized, **D3D12_ERROR_DRIVER_VERSION_MISMATCH** if the provided data came from an old driver or runtime, and **D3D12_ERROR_ADAPTER_NOT_FOUND** if the data came from different hardware.

If you pass `nullptr` for *pPipelineLibrary* then the runtime still performs the validation of the blob but avoid creating the actual library and returns S_FALSE if the library would have been created.

Also, the feature requires an updated driver, and attempting to use it on old drivers will return DXGI_ERROR_UNSUPPORTED.

## -remarks

A pipeline library enables the following operations.

- Adding pipeline state objects (PSOs) to an existing library object (refer to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12pipelinelibrary-storepipeline">StorePipeline</a>).
- Serializing a PSO library into a contiguous block of memory for disk storage (refer to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12pipelinelibrary-serialize">Serialize</a>).
- De-serializing a PSO library from persistent storage (this is handled by <b>CreatePipelineLibrary</b>).
- Retrieving individual PSOs from the library (refer to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline">LoadComputePipeline</a> and <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline">LoadGraphicsPipeline</a>).

At no point in the lifecycle of a pipeline library is there duplication between PSOs with identical sub-components. 

A recommended solution for managing the lifetime of the provided pointer while only having to ref-count the returned interface is to leverage <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface">ID3D12Object::SetPrivateDataInterface</a>, and use an object which implements <b>IUnknown</b>, and frees the memory when the ref-count reaches 0. 

### Thread Safety

The pipeline library is thread-safe to use, and will internally synchronize as necessary, with one exception: multiple threads loading the same PSO (via [**LoadComputePipeline**](nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline.md),
[**LoadGraphicsPipeline**](nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline.md), or [**LoadPipeline**](nf-d3d12-id3d12pipelinelibrary1-loadpipeline.md)) should synchronize themselves, as this act may modify the state of that pipeline within the library in a non-thread-safe manner.

## Examples

See the [Direct3D 12 pipeline state cache sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12PipelineStateCache).

## -see-also

* <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>
* [Direct3D 12 pipeline state cache sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12PipelineStateCache)
