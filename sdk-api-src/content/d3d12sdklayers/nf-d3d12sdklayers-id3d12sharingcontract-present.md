---
UID: NF:d3d12sdklayers.ID3D12SharingContract.Present
title: ID3D12SharingContract::Present
author: windows-sdk-content
description: Shares a resource (or subresource) between the D3D layers and diagnostics tools.
old-location: direct3d12\id3d12sharingcontract_present.htm
old-project: direct3d12
ms.assetid: 878442E3-417A-46CE-B91A-698CA3CA60BE
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12SharingContract interface,Present method, ID3D12SharingContract.Present, ID3D12SharingContract::Present, Present, Present method, Present method,ID3D12SharingContract interface, d3d12sdklayers/ID3D12SharingContract::Present, direct3d12.id3d12sharingcontract_present
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>*</b>

A pointer to the resource to share.


### -param Subresource

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

An unsigned 32bit subresource id.


### -param window






## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt813616(v=VS.85).aspx">ID3D12SharingContract</a>
 

 

