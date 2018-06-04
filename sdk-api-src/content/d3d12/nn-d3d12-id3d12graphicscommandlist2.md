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

# ID3D12GraphicsCommandList2 interface


## -description


Encapsulates a list of graphics commands for rendering, extending the interface to support writing immediate values directly to a buffer.
<div class="alert"><b>Note</b>  This interface was introduced in the Windows 10 Fall Creators Update, and  as such is the latest version of the <b>ID3D12GraphicsCommandList</b> interface. Applications targeting the Windows 10 Fall Creators Update and later should use this interface instead of <a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a> or <a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList2</b> interface inherits from <a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a>. <b>ID3D12GraphicsCommandList2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB1FD3E0-5785-40D1-961B-AF22F9911653">WriteBufferImmediate</a>
</td>
<td align="left" width="63%">
Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a>
 

 

