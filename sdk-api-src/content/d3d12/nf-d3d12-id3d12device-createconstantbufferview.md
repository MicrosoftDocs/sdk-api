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

# ID3D12Device::CreateConstantBufferView


## -description


Creates a constant-buffer view for accessing resource data.


## -parameters




### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/83A4522E-AE87-42CE-9B95-CF63E92556AD">D3D12_CONSTANT_BUFFER_VIEW_DESC</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/83A4522E-AE87-42CE-9B95-CF63E92556AD">D3D12_CONSTANT_BUFFER_VIEW_DESC</a> structure that describes the constant-buffer view.
          


### -param DestDescriptor [in]

Type: <b><a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>


            Describes the CPU descriptor handle that represents the start of the heap that holds the constant-buffer view.
          


## -returns




            Returns nothing.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

