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

# _LUID structure


## -description


Describes a local identifier for an adapter.


## -struct-fields




### -field LowPart

Specifies a DWORD that contains the unsigned lower numbers of the id.


### -field HighPart

Specifies a LONG that contains the signed high numbers of the id.


## -remarks




          This structure is used by the <a href="https://msdn.microsoft.com/006E72E0-AE09-4834-9ACB-D48698050BF2">ID3D12Device::GetAdapterLuid</a> and <a href="https://msdn.microsoft.com/278F1C2B-6DE7-4D4A-8C6E-10B1004B8EFC">GetSharedResourceAdapterLuid</a> methods.
        




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

