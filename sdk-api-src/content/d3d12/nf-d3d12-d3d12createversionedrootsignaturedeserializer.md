---
UID: NF:d3d12.D3D12CreateVersionedRootSignatureDeserializer
title: D3D12CreateVersionedRootSignatureDeserializer function
author: windows-sdk-content
description: Generates an interface that can return the deserialized data structure, via GetUnconvertedRootSignatureDesc.
old-location: direct3d12\d3d12createversionedrootsignaturedeserializer.htm
tech.root: direct3d12
ms.assetid: 0C079508-C330-4391-82CB-54DAAFBACB87
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12CreateVersionedRootSignatureDeserializer, D3D12CreateVersionedRootSignatureDeserializer function, d3d12/D3D12CreateVersionedRootSignatureDeserializer, direct3d12.d3d12createversionedrootsignaturedeserializer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d12.dll
api_name:
 - D3D12CreateVersionedRootSignatureDeserializer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D12CreateVersionedRootSignatureDeserializer function


## -description


Generates an interface that can return the deserialized data structure, via <a href="https://msdn.microsoft.com/7E21B598-C13B-4418-B5B1-4ADDAA18F9B9">GetUnconvertedRootSignatureDesc</a>.


## -parameters




### -param pSrcData [in]

Type: <b>LPCVOID</b>

A pointer to the source data for the serialized root signature.


### -param SrcDataSizeInBytes [in]

Type: <b>SIZE_T</b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.
          


### -param pRootSignatureDeserializerInterface [in]

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the root signature deserializer interface. See remarks.
          


### -param ppRootSignatureDeserializer [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the root signature deserializer. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



If an application has a serialized root signature already or has a compiled shader that contains a root signature and wants to determine the layout definition, it can call <b>D3D12CreateVersionedRootSignatureDeserializer</b> to generate a <a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a> interface. <a href="https://msdn.microsoft.com/50EB9AC8-D13D-41D3-9E16-AC9871095A72">ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion</a>can return the deserialized data structure
        (<a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a>).
        <b>ID3D12VersionedRootSignatureDeserializer</b> just owns the lifetime of the memory for the deserialized data structure.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature deserializer can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a>) will get the <b>GUID</b> of the interface to a root signature deserializer.
      

The function signature PFN_D3D12_CREATE_ROOT_SIGNATURE_DESERIALIZER is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

This function supercedes <a href="https://msdn.microsoft.com/96E58C9B-569F-41B8-A799-E87D849C045C">D3D12CreateRootSignatureDeserializer</a>.




## -see-also




<a href="https://msdn.microsoft.com/C0F9A52C-483D-40B2-9E1F-CB92ADDC2856">Core Functions</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

