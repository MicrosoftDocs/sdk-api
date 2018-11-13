---
UID: NF:d3d12.D3D12CreateVersionedRootSignatureDeserializer
title: D3D12CreateVersionedRootSignatureDeserializer function
author: windows-sdk-content
description: Generates an interface that can return the deserialized data structure, via GetUnconvertedRootSignatureDesc.
old-location: direct3d12\d3d12createversionedrootsignaturedeserializer.htm
tech.root: direct3d12
ms.assetid: 0C079508-C330-4391-82CB-54DAAFBACB87
ms.author: windowssdkdev
ms.date: 11/12/2018
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


Generates an interface that can return the deserialized data structure, via <a href="https://msdn.microsoft.com/en-us/library/Mt709153(v=VS.85).aspx">GetUnconvertedRootSignatureDesc</a>.


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

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
          




## -remarks



If an application has a serialized root signature already or has a compiled shader that contains a root signature and wants to determine the layout definition, it can call <b>D3D12CreateVersionedRootSignatureDeserializer</b> to generate a <a href="https://msdn.microsoft.com/en-us/library/Mt709151(v=VS.85).aspx">ID3D12VersionedRootSignatureDeserializer</a> interface. <a href="https://msdn.microsoft.com/en-us/library/Mt709152(v=VS.85).aspx">ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion</a>can return the deserialized data structure
        (<a href="https://msdn.microsoft.com/en-us/library/Mt709124(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC1</a>).
        <b>ID3D12VersionedRootSignatureDeserializer</b> just owns the lifetime of the memory for the deserialized data structure.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature deserializer can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/en-us/library/Mt709151(v=VS.85).aspx">ID3D12VersionedRootSignatureDeserializer</a>) will get the <b>GUID</b> of the interface to a root signature deserializer.
      

The function signature PFN_D3D12_CREATE_ROOT_SIGNATURE_DESERIALIZER is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

This function supercedes <a href="https://msdn.microsoft.com/en-us/library/Dn859362(v=VS.85).aspx">D3D12CreateRootSignatureDeserializer</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770456(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859357(v=VS.85).aspx">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt709473(v=VS.85).aspx">Root Signature Version 1.1</a>
 

 

