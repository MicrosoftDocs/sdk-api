---
UID: NF:d2d1effectauthor.ID2D1ComputeInfo.SetResourceTexture
title: ID2D1ComputeInfo::SetResourceTexture
author: windows-sdk-content
description: Sets the resource texture corresponding to the given shader texture index to the given texture resource.
old-location: direct2d\id2d1computeinfo_setresourcetexture.htm
tech.root: direct2d
ms.assetid: 20641E91-15EB-4D64-AE36-DB83103B112E
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1ComputeInfo interface [Direct2D],SetResourceTexture method, ID2D1ComputeInfo.SetResourceTexture, ID2D1ComputeInfo::SetResourceTexture, SetResourceTexture, SetResourceTexture method [Direct2D], SetResourceTexture method [Direct2D],ID2D1ComputeInfo interface, d2d1effectauthor/ID2D1ComputeInfo::SetResourceTexture, direct2d.id2d1computeinfo_setresourcetexture
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
 - ID2D1ComputeInfo.SetResourceTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ComputeInfo::SetResourceTexture


## -description


Sets the resource texture corresponding to the given shader texture index to the given texture resource.  The texture resource must already have been loaded with <a href="https://msdn.microsoft.com/265888DA-03C2-42F0-92D8-FEB542F9BAA4">ID2D1EffectContext::CreateResourceTexture</a> method. This call will fail if the specified index overlaps with any input. The input indices always precede the texture LUT indices.



## -parameters




### -param textureIndex

Type: <b>UINT32</b>

The index to set the resource texture on.


### -param resourceTexture [in]

Type: <b><a href="https://msdn.microsoft.com/516FFBB4-1908-4574-BD4A-884C142204CD">ID2D1ResourceTexture</a>*</b>

The resource texture object to set on the shader texture index.


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
 

 

