---
UID: NF:d2d1.ID2D1Mesh.Open
title: ID2D1Mesh::Open
author: windows-sdk-content
description: Opens the mesh for population.
old-location: direct2d\ID2D1Mesh_Open.htm
tech.root: direct2d
ms.assetid: 7cd0d637-7fcd-45a5-932f-5aa8fb476f68
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1Mesh interface [Direct2D],Open method, ID2D1Mesh.Open, ID2D1Mesh::Open, Open, Open method [Direct2D], Open method [Direct2D],ID2D1Mesh interface, d2d1/ID2D1Mesh::Open, direct2d.ID2D1Mesh_Open
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1Mesh.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Mesh::Open


## -description


Opens the mesh for population.


## -parameters




### -param tessellationSink [out]

Type: <b><a href="https://msdn.microsoft.com/967c702f-d16f-4a8e-ac77-a8bb35afe0a1">ID2D1TessellationSink</a>**</b>

When this method returns, contains a pointer to a pointer to an <a href="https://msdn.microsoft.com/967c702f-d16f-4a8e-ac77-a8bb35afe0a1">ID2D1TessellationSink</a> that is used to populate the mesh. This parameter is passed uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2a58fb5f-2281-4f73-a689-cc1350d13c8b">ID2D1Mesh</a>
 

 

