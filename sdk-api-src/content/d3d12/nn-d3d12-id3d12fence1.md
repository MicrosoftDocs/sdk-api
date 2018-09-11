---
UID: NN:d3d12.ID3D12Fence1
title: ID3D12Fence1
author: windows-sdk-content
description: Represents a fence. This interface extends ID3D12Fence, and supports the retrieval of the flags used to create the original fence.
old-location: direct3d12\id3d12fence1.htm
tech.root: direct3d12
ms.assetid: 292FA25B-7C72-4092-8822-DB15951A8309
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12Fence1, ID3D12Fence1 interface, ID3D12Fence1 interface,described, d3d12/ID3D12Fence1, direct3d12.id3d12fence1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID3D12Fence1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Fence1 interface


## -description


Represents a fence. This interface extends <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>, and supports the retrieval of the flags used to create the original fence.  This new feature is useful primarily for opening shared fences.
<div class="alert"><b>Note</b>  <b>ID3D12Fence1</b> was introduced in the Windows 10 Fall Creators Update, and is the latest version of the <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a> interface. Applications targeting Windows 10 Fall Creators Update and later should use <b>ID3D12Fence1</b> instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Fence1</b> interface inherits from <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>. <b>ID3D12Fence1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Fence1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59FF0D7D-CE1F-49AD-8AFE-8C0E7DE05F36">GetCreationFlags</a>
</td>
<td align="left" width="63%">
Gets the flags used to create the fence represented by the current instance.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B">Fence Based Resource Management</a>



<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12fence</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

