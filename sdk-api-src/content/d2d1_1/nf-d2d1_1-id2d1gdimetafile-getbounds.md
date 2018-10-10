---
UID: NF:d2d1_1.ID2D1GdiMetafile.GetBounds
title: ID2D1GdiMetafile::GetBounds
author: windows-sdk-content
description: Gets the bounds of the metafile, in device-independent pixels (DIPs), as reported in the metafile’s header.
old-location: direct2d\id2d1gdimetafile_getbounds.htm
tech.root: Direct2D
ms.assetid: 59DA5314-2A6C-42B0-A4B8-72F6302B4B0F
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetBounds, GetBounds method [Direct2D], GetBounds method [Direct2D],ID2D1GdiMetafile interface, ID2D1GdiMetafile interface [Direct2D],GetBounds method, ID2D1GdiMetafile.GetBounds, ID2D1GdiMetafile::GetBounds, d2d1_1/ID2D1GdiMetafile::GetBounds, direct2d.id2d1gdimetafile_getbounds
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
 - ID2D1GdiMetafile.GetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GdiMetafile::GetBounds


## -description


 Gets the bounds of the metafile, in device-independent pixels (DIPs), as reported in the metafile’s header.


## -parameters




### -param bounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The bounds, in DIPs, of the metafile.


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
 

 

