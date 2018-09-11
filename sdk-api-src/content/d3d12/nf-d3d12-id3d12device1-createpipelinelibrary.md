---
UID: NF:d3d12.ID3D12Device1.CreatePipelineLibrary
title: ID3D12Device1::CreatePipelineLibrary
author: windows-sdk-content
description: Creates a cached pipeline library.
old-location: direct3d12\id3d12device1_createpipelinelibrary.htm
tech.root: direct3d12
ms.assetid: 572A95A6-A02F-4512-9BDE-2A8CA58A0A27
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CreatePipelineLibrary, CreatePipelineLibrary method, CreatePipelineLibrary method,ID3D12Device1 interface, ID3D12Device1 interface,CreatePipelineLibrary method, ID3D12Device1.CreatePipelineLibrary, ID3D12Device1::CreatePipelineLibrary, d3d12/ID3D12Device1::CreatePipelineLibrary, direct3d12.id3d12device1_createpipelinelibrary
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
 - ID3D12Device1.CreatePipelineLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device1::CreatePipelineLibrary


## -description


Creates a cached pipeline library. By grouping PSOs that are expected to share data together into a library before serializing, there’s less overhead due to metadata, as well as opportunity to avoid redundant or duplicated data from being written to disk.


## -parameters




### -param pLibraryBlob [in]

Type: <b>const void*</b>

 If the input library blob is empty, the initial contents of the library is empty. If the input library blob is not empty, it is validated for integrity, parsed, and the pointer is stored. The pointer provided as input to this method must remain valid for the lifetime of the object returned. For efficiency reasons, the data is not copied. 
	  


### -param BlobLength

Type: <b>SIZE_T</b>

Specifies the length of <i>pLibraryBlob</i> in bytes.


### -param riid

Type: <b>REFIID</b>

Specifies a unique REFIID for the <a href="https://msdn.microsoft.com/7A1D750D-51F1-48F6-9D74-6439A147F1EC">ID3D12PipelineLibrary</a> object. 
	  Typically set this and the following parameter with the macro <code>IID_PPV_ARGS(&amp;Library)</code>, where <i>Library</i> is the name of the object.


### -param ppPipelineLibrary [out]

Type: <b>void**</b>

Returns a pointer to the created library.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the blob is corrupted or unrecognized, D3D12_ERROR_DRIVER_VERSION_MISMATCH if the provided data came from an old driver or runtime, and D3D12_ERROR_ADAPTER_NOT_FOUND if the data came from different hardware.

If you pass nullptr for <i>ppPipelineLibrary</i> then the runtime will still perform the validation of the blob but avoid creating the actual library and returns S_FALSE if the library would have been created.

Also, the feature requires an updated driver, and attempting to use it on old drivers will return DXGI_ERROR_UNSUPPORTED.




## -remarks



A pipeline library enables the following operations.

<ul>
<li>Adding Pipeline State Objects (PSOs) to an existing library object (refer to <a href="https://msdn.microsoft.com/A7847966-4B31-47EA-A5CB-B6576CD2501F">StorePipeline</a>). 

      </li>
<li>Serializing a PSO library into a contiguous block of memory for disk storage (refer to <a href="https://msdn.microsoft.com/en-us/library/Mt709149(v=VS.85).aspx">Serialize</a>).</li>
<li>De-serializing a PSO library from persistent storage (this is handled by <b>CreatePipelineLibrary</b>).</li>
<li>Retrieving individual PSOs from the library (refer to <a href="https://msdn.microsoft.com/en-us/library/Mt709147(v=VS.85).aspx">LoadComputePipeline</a> and <a href="https://msdn.microsoft.com/en-us/library/Mt709148(v=VS.85).aspx">LoadGraphicsPipeline</a>).</li>
</ul>
At no point in the lifecycle of a pipeline library is there duplication between PSOs with identical sub-components. 
      A recommended solution for managing the lifetime of the provided pointer while only having to ref-count the returned interface is to leverage <a href="https://msdn.microsoft.com/en-us/library/Dn788703(v=VS.85).aspx">ID3D12Object::SetPrivateDataInterface</a>, and use an object which implements <b>IUnknown</b>, and frees the memory when the ref-count reaches 0. 


#### Examples

Create a PSO library and add PSOs to it. 
    Note the macro IID_PPV_ARGS expands to become two parameters.

<pre class="syntax" xml:space="preserve"><code>ID3D12Device* Device; 
    VERIFY_SUCCEEDED(D3D12CreateDevice(nullptr, IID_PPV_ARGS(&amp;Device))); 
    ID3D12PipelineState* PSO1, PSO2; 

    // Fill out the PSO descs and then call CreateGraphicsPipelineState or CreateComputePipelineState  

    ID3D12PipelineLibrary* Library; 
    VERIFY_SUCCEEDED(Device-&gt;CreatePipelineLibrary(nullptr, 0, IID_PPV_ARGS(&amp;Library))); 
    VERIFY_SUCCEEDED(Library-&gt;StorePipeline(L“PSO1”, PSO1)); 
    VERIFY_SUCCEEDED(Library-&gt;StorePipeline(L“PSO2”, PSO2)); 
    SIZE_T LibrarySize = Library-&gt;GetSerializedSize(); 
    void* pData = new BYTE[LibrarySize]; 
    VERIFY_SUCCEEDED(Library-&gt;Serialize(LibrarySize, pData)); 

    // Save pData to disk 
    ...
    </code></pre>
Create a PSO library using data loaded off of disk and retrieve PSOs out of it. 
    This time the call to <b>CreatePipelineLibrary</b> de-serializes the library.

<pre class="syntax" xml:space="preserve"><code>
    ID3D12Device* Device; 
    VERIFY_SUCCEEDED(D3D12CreateDevice(nullptr, IID_PPV_ARGS(&amp;Device))); 
    ID3D12PipelineState* PSO1, PSO2; 
    const void* LibraryData; 
    SIZE_T LibraryDataSize; 

    // Load library data from disk  

    ID3D12PipelineLibrary* Library; 
    VERIFY_SUCCEEDED(Device-&gt;CreatePipelineLibrary(LibraryData, LibraryDataSize, IID_PPV_ARGS(&amp;Library))); 
    VERIFY_SUCCEEDED(Library-&gt;LoadGraphicsPipeline(L“PSO1”, IID_PPV_ARGS(&amp;PSO1))); 
    VERIFY_SUCCEEDED(Library-&gt;LoadComputePipeline(L“PSO2”, IID_PPV_ARGS(&amp;PSO2))); </code></pre>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt709132(v=VS.85).aspx">ID3D12Device1</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12PipelineStateCache">Pipleline State Cache sample</a>
 

 

