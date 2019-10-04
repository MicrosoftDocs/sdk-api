---
UID: NF:d3d12sdklayers.ID3D12SharingContract.Present
title: ID3D12SharingContract::Present (d3d12sdklayers.h)
author: windows-sdk-content
description: Shares a resource (or subresource) between the D3D layers and diagnostics tools.
old-location: direct3d12\id3d12sharingcontract_present.htm
tech.root: direct3d12
ms.assetid: 878442E3-417A-46CE-B91A-698CA3CA60BE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12SharingContract interface,Present method, ID3D12SharingContract.Present, ID3D12SharingContract::Present, Present, Present method, Present method,ID3D12SharingContract interface, d3d12sdklayers/ID3D12SharingContract::Present, direct3d12.id3d12sharingcontract_present
ms.topic: method
f1_keywords: 
 - "d3d12sdklayers/ID3D12SharingContract.Present"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12SharingContract.Present
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12SharingContract::Present

## -description

Notifies diagnostic tools about an end-of-frame operation without the use of a swap chain. Calling this API enables usage of tools like PIX with applications that either don't render to a window, or that do so in non-traditional ways.

## -parameters

### -param pResource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the resource that contains the final frame contents. This resource is treated as the *back buffer* of the **Present**.

### -param Subresource

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned 32bit subresource id.

### -param window

If provided, indicates which window the tools should use for displaying additional diagnostic information.

## -returns

This method doesn't return a value.

## -see-also

[ID3D12SharingContract](https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract)
