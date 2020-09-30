---
UID: NN:d3d12.ID3D12Device1
title: ID3D12Device1 (d3d12.h)
description: Represents a virtual adapter, and expands on the range of methods provided by ID3D12Device.
helpviewer_keywords: ["ID3D12Device1","ID3D12Device1 interface","ID3D12Device1 interface","described","d3d12/ID3D12Device1","direct3d12.id3d12device1"]
old-location: direct3d12\id3d12device1.htm
tech.root: direct3d12
ms.assetid: 7650C695-3F46-405A-9976-A4A50FFAD567
ms.date: 12/05/2018
ms.keywords: ID3D12Device1, ID3D12Device1 interface, ID3D12Device1 interface,described, d3d12/ID3D12Device1, direct3d12.id3d12device1
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device1
 - d3d12/ID3D12Device1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device1
---

# ID3D12Device1 interface


## -description

Represents a virtual adapter, and expands on the range of methods provided by <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>.
<div class="alert"><b>Note</b>  This interface was introduced in Windows 10 Anniversary Update. Applications targetting Windows 10 Anniversary Update should use this interface instead of earlier or later versions. Applications targetting an earlier or later version of Windows 10 should use the appropriate version of the <b>ID3D12Device</b> interface.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Device1</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>. <b>ID3D12Device1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary">CreatePipelineLibrary</a>
</td>
<td align="left" width="63%">
Creates a cached pipeline library. By grouping PSOs that are expected to share data together into a library before serializing, there’s less overhead due to metadata, as well as opportunity to avoid redundant or duplicated data from being written to disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion">SetEventOnMultipleFenceCompletion</a>
</td>
<td align="left" width="63%">
Specifies an event that should be fired when one or more of a collection of fences reach specific values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority">SetResidencyPriority</a>
</td>
<td align="left" width="63%">
This method sets residency priorities of a specified list of objects.

</td>
</tr>
</table>

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice">D3D12CreateDevice</a> to create a device.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>