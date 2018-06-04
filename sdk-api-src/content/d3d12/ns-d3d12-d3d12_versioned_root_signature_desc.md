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

# D3D12_VERSIONED_ROOT_SIGNATURE_DESC structure


## -description


Holds any version of a root signature description, and is designed to be used with serialization/deserialization functions.


## -struct-fields




### -field Version

Specifies one member of D3D_ROOT_SIGNATURE_VERSION that determines the contents of the union.


### -field Desc_1_0

Specifies a <a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a> (version 1.0).


### -field Desc_1_1

Specifies a <a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a> (version 1.1).


## -remarks



Use this structure with the following methods.

<ul>
<li>
<a href="https://msdn.microsoft.com/50EB9AC8-D13D-41D3-9E16-AC9871095A72">GetRootSignatureDescAtVersion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7E21B598-C13B-4418-B5B1-4ADDAA18F9B9">GetUnconvertedRootSignatureDesc</a>
</li>
<li>
<a href="https://msdn.microsoft.com/D8A15561-4911-4067-B25E-8BF2B079FD81">D3D12SerializeVersionedRootSignature</a>
</li>
</ul>
Refer to the helper structure <a href="https://msdn.microsoft.com/4505C1CE-CAA5-4092-B990-75740A2B194C">CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC</a>. 




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

