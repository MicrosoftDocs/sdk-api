---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the blob is corrupted or unrecognized, D3D12_ERROR_DRIVER_VERSION_MISMATCH if the provided data came from an old driver or runtime, and D3D12_ERROR_ADAPTER_NOT_FOUND if the data came from different hardware.

If you pass nullptr for <i>ppPipelineLibrary</i> then the runtime will still perform the validation of the blob but avoid creating the actual library and returns S_FALSE if the library would have been created.

Also, the feature requires an updated driver, and attempting to use it on old drivers will return DXGI_ERROR_UNSUPPORTED.




## -remarks



A pipeline library enables the following operations.

<ul>
<li>Adding Pipeline State Objects (PSOs) to an existing library object (refer to <a href="https://msdn.microsoft.com/A7847966-4B31-47EA-A5CB-B6576CD2501F">StorePipeline</a>). 

      </li>
<li>Serializing a PSO library into a contiguous block of memory for disk storage (refer to <a href="https://msdn.microsoft.com/FD81B464-1E93-47CF-9D95-8F8F64C39CD6">Serialize</a>).</li>
<li>De-serializing a PSO library from persistent storage (this is handled by <b>CreatePipelineLibrary</b>).</li>
<li>Retrieving individual PSOs from the library (refer to <a href="https://msdn.microsoft.com/8295D6E3-8353-46AD-A741-170244495F8B">LoadComputePipeline</a> and <a href="https://msdn.microsoft.com/1DDD1348-2039-4BF4-9ED8-7AA087D0B654">LoadGraphicsPipeline</a>).</li>
</ul>
At no point in the lifecycle of a pipeline library is there duplication between PSOs with identical sub-components. 
      A recommended solution for managing the lifetime of the provided pointer while only having to ref-count the returned interface is to leverage <a href="https://msdn.microsoft.com/B03B9420-7E85-4C1A-858C-37B20E4D9B52">ID3D12Object::SetPrivateDataInterface</a>, and use an object which implements <b>IUnknown</b>, and frees the memory when the ref-count reaches 0. 


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




<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12PipelineStateCache">Pipleline State Cache sample</a>
 

 

