---
UID: NF:d3d12.ID3D12Device5.CreateStateObject
title: ID3D12Device5::CreateStateObject
author: windows-sdk-content
description: Creates an ID3D12StateObject.
old-location: direct3d12\id3d12device5_createstateobject.htm
tech.root: direct3d12
ms.assetid: 9CC759D5-6414-4B05-B8F3-FA6056A0A9AF
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateStateObject, CreateStateObject method, CreateStateObject method,ID3D12Device5 interface, ID3D12Device5 interface,CreateStateObject method, ID3D12Device5.CreateStateObject, ID3D12Device5::CreateStateObject, d3d12/ID3D12Device5::CreateStateObject, direct3d12.id3d12device5_createstateobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device5.CreateStateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12Device5.CreateStateObject
: 
---

# ID3D12Device5::CreateStateObject


## -description


Creates an <a href="https://msdn.microsoft.com/5BE94583-31DC-4469-9049-7768D64F7F41">ID3D12StateObject</a>.


## -parameters




### -param pDesc [in]

The description of the state object to create.


### -param riid

The GUID of the interface to create. Use <i>__uuidof(ID3D12StateObject)</i>.


### -param ppStateObject [out]

The returned state object.


## -returns



Returns S_OK if successful; otherwise, returns one of the following values:
              

<ul>
<li>E_INVALIDARG if one of the input parameters is invalid.</li>
<li>E_OUTOFMEMORY if sufficient memory is not available to create the handle.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> topic.
              </li>
</ul>



## -see-also




<a href="direct3d12.id3d122device">ID3D122Device</a>



<a href="https://msdn.microsoft.com/2D72898B-F512-4E0D-8FAC-A53EA6FE614A">ID3D12Device5</a>
 

 

