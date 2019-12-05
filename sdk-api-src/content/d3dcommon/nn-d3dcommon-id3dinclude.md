---
UID: NN:d3dcommon.ID3DInclude
title: ID3DInclude (d3dcommon.h)
description: ID3DInclude is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader
old-location: direct3d11\id3dinclude.htm
tech.root: direct3d11
ms.assetid: 2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5
ms.date: 12/05/2018
ms.keywords: ID3DInclude, ID3DInclude interface [Direct3D 11], ID3DInclude interface [Direct3D 11],described, d3dcommon/ID3DInclude, direct3d11.id3dinclude
ms.topic: interface
f1_keywords:
- d3dcommon/ID3DInclude
dev_langs:
- c++
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCompiler_47.dll
api_name:
- ID3DInclude
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3DInclude interface


## -description


<b>ID3DInclude</b> is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader #include files.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DInclude</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DInclude</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DInclude</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-close">Close</a>
</td>
<td align="left" width="63%">
A user-implemented method for closing a shader #include file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3dcommon/nf-d3dcommon-id3dinclude-open">Open</a>
</td>
<td align="left" width="63%">
A user-implemented method for opening and reading the contents of a shader #include file.

</td>
</tr>
</table> 


## -remarks



To use this interface, create an interface that inherits from <b>ID3DInclude</b> and implement custom behavior for the methods.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-interfaces">Common Version Interfaces</a>
 

 

