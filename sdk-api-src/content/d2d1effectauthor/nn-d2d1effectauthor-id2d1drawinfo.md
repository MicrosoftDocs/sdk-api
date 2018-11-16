---
UID: NN:d2d1effectauthor.ID2D1DrawInfo
title: ID2D1DrawInfo
author: windows-sdk-content
description: This interface is used to describe a GPU rendering pass on a vertex or pixel shader. It is passed to ID2D1DrawTransform.
old-location: direct2d\id2d1drawinfo.htm
tech.root: Direct2D
ms.assetid: 9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1DrawInfo, ID2D1DrawInfo interface [Direct2D], ID2D1DrawInfo interface [Direct2D],described, d2d1effectauthor/ID2D1DrawInfo, direct2d.id2d1drawinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID2D1DrawInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo interface


## -description


This interface is used to describe a GPU rendering pass on a vertex or pixel shader. It is passed to <a href="https://msdn.microsoft.com/90C49A9A-9297-44E6-9AB8-01C6847CA3F8">ID2D1DrawTransform</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DrawInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1DrawInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DrawInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9CB38592-6B49-48FE-AA3F-1FC402489454">SetPixelShader</a>
</td>
<td align="left" width="63%">
Set the shader instructions for this transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A32E831-3754-4EF5-B559-ED02EF747897">SetPixelShaderConstantBuffer</a>
</td>
<td align="left" width="63%">
Sets the constant buffer for this transform's pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E53577B-AD97-4530-8260-4A99B90E0581">SetResourceTexture</a>
</td>
<td align="left" width="63%">
Sets the resource texture corresponding to the given shader texture index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23DB679B-33E4-4FB1-B356-BBB1BA95E0EB">SetVertexProcessing</a>
</td>
<td align="left" width="63%">
Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A7991C9-BB3F-4E58-9FA7-5C4B194C33F6">SetVertexShaderConstantBuffer</a>
</td>
<td align="left" width="63%">
Sets the constant buffer for this transform's vertex shader.

</td>
</tr>
</table> 

