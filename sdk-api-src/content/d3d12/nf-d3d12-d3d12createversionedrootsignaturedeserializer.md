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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




        If an application has a serialized root signature already or has a compiled shader that contains a root signature and wants to determine the layout definition, it can call <b>D3D12CreateVersionedRootSignatureDeserializer</b> to generate a <a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a> interface. <a href="https://msdn.microsoft.com/50EB9AC8-D13D-41D3-9E16-AC9871095A72">ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion</a>
        can return the deserialized data structure
        (<a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a>).
        <b>ID3D12VersionedRootSignatureDeserializer</b> just owns the lifetime of the memory for the deserialized data structure.
      


        The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature deserializer can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a>) will get the <b>GUID</b> of the interface to a root signature deserializer.
      


        The function signature PFN_D3D12_CREATE_ROOT_SIGNATURE_DESERIALIZER is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

This function supercedes <a href="https://msdn.microsoft.com/96E58C9B-569F-41B8-A799-E87D849C045C">D3D12CreateRootSignatureDeserializer</a>.




## -see-also




<a href="https://msdn.microsoft.com/C0F9A52C-483D-40B2-9E1F-CB92ADDC2856">Core Functions</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

