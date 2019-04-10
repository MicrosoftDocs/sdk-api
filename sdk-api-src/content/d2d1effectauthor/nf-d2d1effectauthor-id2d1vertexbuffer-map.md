---
UID: NF:d2d1effectauthor.ID2D1VertexBuffer.Map
title: ID2D1VertexBuffer::Map (d2d1effectauthor.h)
author: windows-sdk-content
description: Maps the provided data into user memory.
old-location: direct2d\id2d1vertexbuffer_map.htm
tech.root: Direct2D
ms.assetid: 3EFC0584-2F03-4B35-8C6C-E46CDD9D9057
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1VertexBuffer interface [Direct2D],Map method, ID2D1VertexBuffer.Map, ID2D1VertexBuffer::Map, Map, Map method [Direct2D], Map method [Direct2D],ID2D1VertexBuffer interface, d2d1effectauthor/ID2D1VertexBuffer::Map, direct2d.id2d1vertexbuffer_map
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
 - ID2D1VertexBuffer.Map
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1VertexBuffer::Map


## -description


Maps the provided data into user memory.


## -parameters




### -param data [out]

Type: <b>const BYTE**</b>

When this method returns, contains the address of a pointer to the available buffer.


### -param bufferSize

Type: <b>UINT32</b>

The desired size of the buffer.


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
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D3DERR_DEVICELOST</td>
<td>The device has been lost but cannot be reset at this time.</td>
</tr>
</table>
 






## -remarks



If <i>data</i> is larger than <i>bufferSize</i>, this method fails.
      




## -see-also




<a href="https://msdn.microsoft.com/8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/1DBCDF93-83C6-4B02-9E94-8024D7849DF7">ID2D1VertexBuffer</a>
 

 

