---
UID: NF:d3d10.ID3D10Buffer.Unmap
title: ID3D10Buffer::Unmap
author: windows-sdk-content
description: Invalidate the pointer to the resource retrieved by ID3D10Buffer::Map and reenable GPU access to the resource.
old-location: direct3d10\id3d10buffer_unmap.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer_unmap.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 13d21090-d886-01c2-e3ba-12169dea4cc5, ID3D10Buffer interface [Direct3D 10],Unmap method, ID3D10Buffer.Unmap, ID3D10Buffer::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Buffer interface, d3d10/ID3D10Buffer::Unmap, direct3d10.id3d10buffer_unmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Buffer.Unmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Buffer::Unmap


## -description


Invalidate the pointer to the resource retrieved by <a href="https://msdn.microsoft.com/en-us/library/Bb173512(v=VS.85).aspx">ID3D10Buffer::Map</a> and reenable GPU access to the resource.


## -parameters






## -returns



Returns nothing




## -remarks



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer Interface</a>
 

 

