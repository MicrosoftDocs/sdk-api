---
UID: NF:d2d1_1.ID2D1GdiMetafile.Stream
title: ID2D1GdiMetafile::Stream
author: windows-sdk-content
description: This method streams the contents of the command to the given metafile sink.
old-location: direct2d\id2d1gdimetafile_stream.htm
tech.root: direct2d
ms.assetid: 84E7305D-1E2D-43C3-8E79-02EBCC8F36A1
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1GdiMetafile interface [Direct2D],Stream method, ID2D1GdiMetafile.Stream, ID2D1GdiMetafile::Stream, Stream, Stream method [Direct2D], Stream method [Direct2D],ID2D1GdiMetafile interface, d2d1_1/ID2D1GdiMetafile::Stream, direct2d.id2d1gdimetafile_stream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
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
req.lib: 
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
 - ID2D1GdiMetafile.Stream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GdiMetafile::Stream


## -description


This method streams the contents of the command  to the given metafile  sink. 


## -parameters




### -param sink

TBD




#### - metafileSink

Type: <b><a href="https://msdn.microsoft.com/1E9866C3-2A07-48C2-A4C5-F9AE3C7B2272">ID2D1GdiMetafileSink</a></b>

The sink into which Direct2D  will call back.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a>
 

 

