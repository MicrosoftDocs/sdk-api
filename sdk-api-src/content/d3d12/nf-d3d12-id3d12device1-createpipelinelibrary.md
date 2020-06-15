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
f1_keywords:
- d3d12/ID3D12Device1.CreatePipelineLibrary
dev_langs:
- c++
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
- ID3D12Device1.CreatePipelineLibrary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device1::CreatePipelineLibrary

## -description

Creates a cached pipeline library. For pipeline state objects (PSOs) that are expected to share data together, grouping them into a library before serializing them means that there's less overhead due to metadata, as well as the opportunity to avoid redundant or duplicated data from being written to disk.

## -parameters

### -param pLibraryBlob [in]

Type: **const void\***

If the input library blob is empty, then the initial content of the library is empty. If the input library blob is not empty, then it is validated for integrity, parsed, and the pointer is stored. The pointer provided as input to this method must remain valid for the lifetime of the object returned. For efficiency reasons, the data is not copied. 

### -param BlobLength

Type: **[SIZE_T](/windows/desktop/winprog/windows-data-types)**

Specifies the length of *pLibraryBlob* in bytes.

### -param riid

Type: **REFIID**

Specifies a unique REFIID for the [ID3D12PipelineLibrary](/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinelibrary) object. Typically set this and the following parameter with the macro `IID_PPV_ARGS(&Library)`, where **Library** is the name of the object.

### -param ppPipelineLibrary [out]

Type: **void\*\***

Returns a pointer to the created library.

## -returns
Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10), including E_INVALIDARG if the blob is corrupted or unrecognized, D3D12_ERROR_DRIVER_VERSION_MISMATCH if the provided data came from an old driver or runtime, and D3D12_ERROR_ADAPTER_NOT_FOUND if the data came from different hardware.

If you pass `nullptr` for *pPipelineLibrary* then the runtime still performs the validation of the blob but avoid creating the actual library and returns S_FALSE if the library would have been created.

Also, the feature requires an updated driver, and attempting to use it on old drivers will return DXGI_ERROR_UNSUPPORTED.

## -remarks

A pipeline library enables the following operations.

- Adding pipeline state objects (PSOs) to an existing library object (refer to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-storepipeline">StorePipeline</a>).
- Serializing a PSO library into a contiguous block of memory for disk storage (refer to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-serialize">Serialize</a>).
- De-serializing a PSO library from persistent storage (this is handled by <b>CreatePipelineLibrary</b>).
- Retrieving individual PSOs from the library (refer to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline">LoadComputePipeline</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline">LoadGraphicsPipeline</a>).

At no point in the lifecycle of a pipeline library is there duplication between PSOs with identical sub-components. 

A recommended solution for managing the lifetime of the provided pointer while only having to ref-count the returned interface is to leverage <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setprivatedatainterface">ID3D12Object::SetPrivateDataInterface</a>, and use an object which implements <b>IUnknown</b>, and frees the memory when the ref-count reaches 0. 

#### Thread Safety

The pipeline library is thread-safe to use, and will internally synchronize as necessary, with one exception: multiple threads loading the same PSO (via [**LoadComputePipeline**](nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline.md),
[**LoadGraphicsPipeline**](nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline.md), or [**LoadPipeline**](nf-d3d12-id3d12pipelinelibrary1-loadpipeline.md)) should synchronize themselves, as this act may modify the state of that pipeline within the library in a non-thread-safe manner.

#### Examples

Create a PSO library and add PSOs to it. Note the macro IID_PPV_ARGS expands to become two parameters.

```cpp
ID3D12Device* Device; 
    VERIFY_SUCCEEDED(D3D12CreateDevice(nullptr, IID_PPV_ARGS(&Device))); 
    ID3D12PipelineState* PSO1, PSO2; 

    // Fill out the PSO descs and then call CreateGraphicsPipelineState or CreateComputePipelineState  

    ID3D12PipelineLibrary* Library; 
    VERIFY_SUCCEEDED(Device->CreatePipelineLibrary(nullptr, 0, IID_PPV_ARGS(&Library))); 
    VERIFY_SUCCEEDED(Library->StorePipeline(L“PSO1”, PSO1)); 
    VERIFY_SUCCEEDED(Library->StorePipeline(L“PSO2”, PSO2)); 
    SIZE_T LibrarySize = Library->GetSerializedSize(); 
    void* pData = new BYTE[LibrarySize]; 
    VERIFY_SUCCEEDED(Library->Serialize(pData, LibrarySize)); 

    // Save pData to disk 
    ...
```

Create a PSO library using data loaded off of disk and retrieve PSOs out of it. This time the call to <b>CreatePipelineLibrary</b> de-serializes the library.

```cpp
    ID3D12Device* Device; 
    VERIFY_SUCCEEDED(D3D12CreateDevice(nullptr, IID_PPV_ARGS(&Device))); 
    ID3D12PipelineState* PSO1, PSO2; 
    const void* LibraryData; 
    SIZE_T LibraryDataSize; 

    // Load library data from disk  

    ID3D12PipelineLibrary* Library; 
    VERIFY_SUCCEEDED(Device->CreatePipelineLibrary(LibraryData, LibraryDataSize, IID_PPV_ARGS(&Library))); 
    VERIFY_SUCCEEDED(Library->LoadGraphicsPipeline(L“PSO1”, IID_PPV_ARGS(&PSO1))); 
    VERIFY_SUCCEEDED(Library->LoadComputePipeline(L“PSO2”, IID_PPV_ARGS(&PSO2)));
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>, <a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12PipelineStateCache">Pipleline State Cache sample</a>
