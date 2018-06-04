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

# ID3D12Device1::SetEventOnMultipleFenceCompletion


## -description


Specifies an event that should be fired when one or more of a collection of fences reach specific values.


## -parameters




### -param ppFences [in]

Type: <b>ID3D12Fence*</b>

An array of length <i>NumFences</i> that specifies the <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a> objects.


### -param pFenceValues [in]

Type: <b>const UINT64*</b>

An array of length <i>NumFences</i> that specifies the fence values required for the event is to be signaled.


### -param NumFences

Type: <b>UINT</b>

Specifies the number of fences to be included.


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/A5C52F58-C082-41C2-99E4-800DFBA250D2">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a></b>

Specifies one  of the <a href="https://msdn.microsoft.com/A5C52F58-C082-41C2-99E4-800DFBA250D2">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a> that determines how to proceed.


### -param hEvent

Type: <b>HANDLE</b>

A handle to the event object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



To specify a single fence refer to the <a href="https://msdn.microsoft.com/DBC5A1FD-F3D0-4C9B-965B-1967151093F7">SetEventOnCompletion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>
 

 

