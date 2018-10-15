---
UID: NF:d2d1effectauthor.ID2D1ComputeInfo.SetComputeShader
title: ID2D1ComputeInfo::SetComputeShader
author: windows-sdk-content
description: Sets the compute shader to the given shader resource. The resource must be loaded before this call is made.
old-location: direct2d\id2d1computeinfo_setcomputeshader.htm
tech.root: direct2d
ms.assetid: C5D45B7C-6EC8-4150-B0A9-C936C52B9E58
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID2D1ComputeInfo interface [Direct2D],SetComputeShader method, ID2D1ComputeInfo.SetComputeShader, ID2D1ComputeInfo::SetComputeShader, SetComputeShader, SetComputeShader method [Direct2D], SetComputeShader method [Direct2D],ID2D1ComputeInfo interface, d2d1effectauthor/ID2D1ComputeInfo::SetComputeShader, direct2d.id2d1computeinfo_setcomputeshader
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
 - d2d1.dll
api_name:
 - ID2D1ComputeInfo.SetComputeShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ComputeInfo::SetComputeShader


## -description


Sets the compute shader to the given shader resource.  The resource must be loaded before this call is made.


## -parameters




### -param shaderId [in]

Type: <b>REFGUID</b>

The GUID of the shader.


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
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0560BB4B-B837-4DA8-AD68-545224152BA5">ID2D1ComputeInfo</a>
 

 

