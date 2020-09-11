---
UID: NN:d3d11.ID3D11ClassInstance
title: ID3D11ClassInstance (d3d11.h)
description: This interface encapsulates an HLSL class.
helpviewer_keywords: ["ID3D11ClassInstance","ID3D11ClassInstance interface [Direct3D 11]","ID3D11ClassInstance interface [Direct3D 11]","described","d3d11/ID3D11ClassInstance","direct3d11.id3d11classinstance","fb695194-ccb6-d8bd-59c0-5dbd185a1a4c"]
old-location: direct3d11\id3d11classinstance.htm
tech.root: direct3d11
ms.assetid: 70d006d2-5c47-4e8a-9a14-b5475d88ac32
ms.date: 12/05/2018
ms.keywords: ID3D11ClassInstance, ID3D11ClassInstance interface [Direct3D 11], ID3D11ClassInstance interface [Direct3D 11],described, d3d11/ID3D11ClassInstance, direct3d11.id3d11classinstance, fb695194-ccb6-d8bd-59c0-5dbd185a1a4c
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ClassInstance
 - d3d11/ID3D11ClassInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ClassInstance
---

# ID3D11ClassInstance interface


## -description

This interface encapsulates an HLSL class.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ClassInstance</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11ClassInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ClassInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11classinstance-getclasslinkage">GetClassLinkage</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a> object associated with the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11classinstance-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a description of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11classinstance-getinstancename">GetInstanceName</a>
</td>
<td align="left" width="63%">
Gets the instance name of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11classinstance-gettypename">GetTypeName</a>
</td>
<td align="left" width="63%">
Gets the type of the current HLSL class.

</td>
</tr>
</table>

## -remarks

This interface is created by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance">ID3D11ClassLinkage::CreateClassInstance</a>. The interface is used when binding shader resources to the pipeline using APIs such as <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshader">ID3D11DeviceContext::VSSetShader</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>

