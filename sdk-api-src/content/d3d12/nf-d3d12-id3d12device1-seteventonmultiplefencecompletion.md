---
UID: NF:d3d12.ID3D12Device1.SetEventOnMultipleFenceCompletion
title: ID3D12Device1::SetEventOnMultipleFenceCompletion
author: windows-sdk-content
description: Specifies an event that should be fired when one or more of a collection of fences reach specific values.
old-location: direct3d12\id3d12device1_seteventonmultiplefencecompletion.htm
old-project: direct3d12
ms.assetid: C187EEB7-DCD0-4535-AF0E-EF2C0E2DC83C
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12Device1 interface,SetEventOnMultipleFenceCompletion method, ID3D12Device1.SetEventOnMultipleFenceCompletion, ID3D12Device1::SetEventOnMultipleFenceCompletion, SetEventOnMultipleFenceCompletion, SetEventOnMultipleFenceCompletion method, SetEventOnMultipleFenceCompletion method,ID3D12Device1 interface, d3d12/ID3D12Device1::SetEventOnMultipleFenceCompletion, direct3d12.id3d12device1_seteventonmultiplefencecompletion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
 - ID3D12Device1.SetEventOnMultipleFenceCompletion
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device1::SetEventOnMultipleFenceCompletion


## -description


Specifies an event that should be fired when one or more of a collection of fences reach specific values.


## -parameters




### -param ppFences [in]

Type: <b>ID3D12Fence*</b>

An array of length <i>NumFences</i> that specifies the <a href="https://msdn.microsoft.com/en-us/library/Dn899188(v=VS.85).aspx">ID3D12Fence</a> objects.


### -param pFenceValues [in]

Type: <b>const UINT64*</b>

An array of length <i>NumFences</i> that specifies the fence values required for the event is to be signaled.


### -param NumFences

Type: <b>UINT</b>

Specifies the number of fences to be included.


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt709118(v=VS.85).aspx">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a></b>

Specifies one  of the <a href="https://msdn.microsoft.com/en-us/library/Mt709118(v=VS.85).aspx">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a> that determines how to proceed.


### -param hEvent

Type: <b>HANDLE</b>

A handle to the event object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



To specify a single fence refer to the <a href="https://msdn.microsoft.com/en-us/library/Dn899190(v=VS.85).aspx">SetEventOnCompletion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt709132(v=VS.85).aspx">ID3D12Device1</a>
 

 

