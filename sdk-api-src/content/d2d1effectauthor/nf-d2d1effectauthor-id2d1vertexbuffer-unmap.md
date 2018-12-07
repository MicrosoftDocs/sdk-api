---
UID: NF:d2d1effectauthor.ID2D1VertexBuffer.Unmap
title: ID2D1VertexBuffer::Unmap
author: windows-sdk-content
description: Unmaps the vertex buffer.
old-location: direct2d\id2d1vertexbuffer_unmap.htm
tech.root: direct2d
ms.assetid: DD33E4D4-C020-4830-AD31-380E8E9217D0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1VertexBuffer interface [Direct2D],Unmap method, ID2D1VertexBuffer.Unmap, ID2D1VertexBuffer::Unmap, Unmap, Unmap method [Direct2D], Unmap method [Direct2D],ID2D1VertexBuffer interface, d2d1effectauthor/ID2D1VertexBuffer::Unmap, direct2d.id2d1vertexbuffer_unmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1VertexBuffer.Unmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1VertexBuffer::Unmap


## -description


Unmaps the vertex buffer.


## -parameters






## -returns



Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_WRONG_STATE</td>
<td>The object was not in the correct state to process the method.</td>
</tr>
</table>
 






## -remarks



After this method returns, the mapped memory from the vertex buffer is no longer accessible by the effect.




## -see-also




<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/1DBCDF93-83C6-4B02-9E94-8024D7849DF7">ID2D1VertexBuffer</a>
 

 

