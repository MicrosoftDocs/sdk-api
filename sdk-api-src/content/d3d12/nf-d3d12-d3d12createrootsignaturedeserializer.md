---
UID: NF:d3d12.D3D12CreateRootSignatureDeserializer
title: D3D12CreateRootSignatureDeserializer function
author: windows-sdk-content
description: Deserializes a root signature so you can determine the layout definition (D3D12_ROOT_SIGNATURE_DESC).
old-location: direct3d12\d3d12createrootsignaturedeserializer.htm
old-project: direct3d12
ms.assetid: 96E58C9B-569F-41B8-A799-E87D849C045C
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12CreateRootSignatureDeserializer, D3D12CreateRootSignatureDeserializer function, d3d12/D3D12CreateRootSignatureDeserializer, direct3d12.d3d12createrootsignaturedeserializer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12CreateRootSignatureDeserializer
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# D3D12CreateRootSignatureDeserializer function


## -description


Deserializes a root signature so you can determine the layout definition (<a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a>).
        


## -parameters




### -param pSrcData [in]

Type: <b>LPCVOID</b>

A pointer to the source data for the serialized root signature.


### -param SrcDataSizeInBytes [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.
          


### -param pRootSignatureDeserializerInterface [in]

Type: <b><b>REFIID</b></b>

The globally unique identifier (<b>GUID</b>) for the root signature deserializer interface. See remarks.
          


### -param ppRootSignatureDeserializer [out]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the root signature deserializer. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



This function has been superceded by <a href="https://msdn.microsoft.com/0C079508-C330-4391-82CB-54DAAFBACB87">D3D12CreateVersionedRootSignatureDeserializer</a>.

If an application has a serialized root signature already or has a compiled shader that contains a root signature and wants to determine the layout definition, it can call <b>D3D12CreateRootSignatureDeserializer</b> to generate a <a href="https://msdn.microsoft.com/FEDA0802-45A6-4ED5-9683-5278BD60B7A4">ID3D12RootSignatureDeserializer</a> interface. <a href="https://msdn.microsoft.com/A13FB848-A5C1-4B9B-9009-B0166A3A1C8D">ID3D12RootSignatureDeserializer::GetRootSignature</a>can return the deserialized data structure
        (<a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a>).
        <b>ID3D12RootSignatureDeserializer</b> just owns the lifetime of the memory for the deserialized data structure.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature deserializer can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/FEDA0802-45A6-4ED5-9683-5278BD60B7A4">ID3D12RootSignatureDeserializer</a>) will get the <b>GUID</b> of the interface to a root signature deserializer.
      

The function signature PFN_D3D12_CREATE_ROOT_SIGNATURE_DESERIALIZER is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      




## -see-also




<a href="https://msdn.microsoft.com/C0F9A52C-483D-40B2-9E1F-CB92ADDC2856">Core Functions</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>
 

 

