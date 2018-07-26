---
UID: NF:d3d12sdklayers.ID3D12SharingContract.Present
title: ID3D12SharingContract::Present
author: windows-sdk-content
description: Shares a resource (or subresource) between the D3D layers and diagnostics tools.
old-location: direct3d12\id3d12sharingcontract_present.htm
old-project: direct3d12
ms.assetid: 878442E3-417A-46CE-B91A-698CA3CA60BE
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12SharingContract interface,Present method, ID3D12SharingContract.Present, ID3D12SharingContract::Present, Present, Present method, Present method,ID3D12SharingContract interface, d3d12sdklayers/ID3D12SharingContract::Present, direct3d12.id3d12sharingcontract_present
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12SharingContract.Present
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12SharingContract::Present


## -description


Shares a resource (or subresource) between the D3D layers and diagnostics tools.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>*</b>

A pointer to the resource to share.


### -param Subresource

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned 32bit subresource id.


### -param window






## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/10E61C88-0CDC-42E6-AB70-4911D254C40A">ID3D12SharingContract</a>
 

 

