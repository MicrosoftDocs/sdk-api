---
UID: NN:d2d1effectauthor.ID2D1DrawInfo
title: ID2D1DrawInfo (d2d1effectauthor.h)
author: windows-sdk-content
description: This interface is used to describe a GPU rendering pass on a vertex or pixel shader. It is passed to ID2D1DrawTransform.
old-location: direct2d\id2d1drawinfo.htm
tech.root: Direct2D
ms.assetid: 9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1DrawInfo, ID2D1DrawInfo interface [Direct2D], ID2D1DrawInfo interface [Direct2D],described, d2d1effectauthor/ID2D1DrawInfo, direct2d.id2d1drawinfo
ms.topic: interface
f1_keywords: ["d2d1effectauthor/ID2D1DrawInfo"]
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
ms.custom: 19H1
---

# ID2D1DrawInfo interface


## -description


This interface is used to describe a GPU rendering pass on a vertex or pixel shader. It is passed to <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform">ID2D1DrawTransform</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DrawInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1DrawInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshader">SetPixelShader</a>
</td>
<td align="left" width="63%">
Set the shader instructions for this transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer">SetPixelShaderConstantBuffer</a>
</td>
<td align="left" width="63%">
Sets the constant buffer for this transform's pixel shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setresourcetexture">SetResourceTexture</a>
</td>
<td align="left" width="63%">
Sets the resource texture corresponding to the given shader texture index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing">SetVertexProcessing</a>
</td>
<td align="left" width="63%">
Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexshaderconstantbuffer">SetVertexShaderConstantBuffer</a>
</td>
<td align="left" width="63%">
Sets the constant buffer for this transform's vertex shader.

</td>
</tr>
</table> 

