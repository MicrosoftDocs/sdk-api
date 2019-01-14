---
UID: NF:d2d1.ID2D1TessellationSink.AddTriangles
title: ID2D1TessellationSink::AddTriangles
author: windows-sdk-content
description: Copies the specified triangles to the sink.
old-location: direct2d\ID2D1TessellationSink_AddTriangles.htm
tech.root: Direct2D
ms.assetid: 45084e57-d022-4bdb-9001-83e4e88c9c55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddTriangles, AddTriangles method [Direct2D], AddTriangles method [Direct2D],ID2D1TessellationSink interface, ID2D1TessellationSink interface [Direct2D],AddTriangles method, ID2D1TessellationSink.AddTriangles, ID2D1TessellationSink::AddTriangles, d2d1/ID2D1TessellationSink::AddTriangles, direct2d.ID2D1TessellationSink_AddTriangles
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1TessellationSink.AddTriangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TessellationSink::AddTriangles


## -description


Copies the specified triangles to the sink. 


## -parameters




### -param triangles [in]

Type: <b>const <a href="https://msdn.microsoft.com/6978bfff-05ca-44b6-8694-c4741f7987f6">D2D1_TRIANGLE</a>*</b>

An array of <a href="https://msdn.microsoft.com/6978bfff-05ca-44b6-8694-c4741f7987f6">D2D1_TRIANGLE</a> structures that describe the triangles to add to the sink.


### -param trianglesCount

Type: <b>UINT</b>

The number of triangles to copy from the <i>triangles</i> array.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/967c702f-d16f-4a8e-ac77-a8bb35afe0a1">ID2D1TessellationSink</a>
 

 

