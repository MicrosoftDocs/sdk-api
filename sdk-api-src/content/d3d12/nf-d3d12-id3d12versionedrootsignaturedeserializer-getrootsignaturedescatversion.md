---
UID: NF:d3d12.ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion
title: ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion
author: windows-sdk-content
description: Converts root signature description structures to a requested version.
old-location: direct3d12\id3d12versionedrootsignaturedeserializer_getrootsignaturedescatversion.htm
old-project: direct3d12
ms.assetid: 50EB9AC8-D13D-41D3-9E16-AC9871095A72
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetRootSignatureDescAtVersion, GetRootSignatureDescAtVersion method, GetRootSignatureDescAtVersion method,ID3D12VersionedRootSignatureDeserializer interface, ID3D12VersionedRootSignatureDeserializer interface,GetRootSignatureDescAtVersion method, ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion, ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion, d3d12/ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion, direct3d12.id3d12versionedrootsignaturedeserializer_getrootsignaturedescatversion
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion


## -description


Converts root signature description structures to a requested version.


## -parameters




### -param convertToVersion

Type: <b><a href="https://msdn.microsoft.com/44A22509-5CAE-4C4E-ADC6-E86B5BD8CE3B">D3D_ROOT_SIGNATURE_VERSION</a></b>

Specifies the required <a href="https://msdn.microsoft.com/44A22509-5CAE-4C4E-ADC6-E86B5BD8CE3B">D3D_ROOT_SIGNATURE_VERSION</a>.


### -param ppDesc [out]

Type: <b>const <a href="https://msdn.microsoft.com/46F692DD-55FF-4DFF-AF11-78CAD10922C1">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>**</b>

Contains the deserialized root signature in a  <a href="https://msdn.microsoft.com/46F692DD-55FF-4DFF-AF11-78CAD10922C1">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> structure.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code. The method can fail with E_OUTOFMEMORY.




## -remarks



This method allocates additional storage if needed for the converted root signature (memory owned by the deserializer interface).  If conversion is done, the deserializer interface doesn’t free the original deserialized root signature memory – all versions the interface has been asked to convert to are available until the deserializer is destroyed. 

Converting a root signature from 1.1 to 1.0 will drop all <a href="https://msdn.microsoft.com/B22DBE80-A0BE-40F9-ADC2-5AFB35DDDDE8">D3D12_DESCRIPTOR_RANGE_FLAGS</a> and <a href="https://msdn.microsoft.com/1BF4D1FA-C938-4704-8D82-CFCA6FE954CB">D3D12_ROOT_DESCRIPTOR_FLAGS</a> can be useful for generating compatible root signatures that need to run on old operating systems, though does lose optimization opportunities.  For instance, multiple root signature versions can be serialized and stored with application assets, with the appropriate version used at runtime based on the operating system capabilities.  

Converting a root signature from 1.0 to 1.1 just adds the appropriate flags to match 1.0 semantics.




## -see-also




<a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

