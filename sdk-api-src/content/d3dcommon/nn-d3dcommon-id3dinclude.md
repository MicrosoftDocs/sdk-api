---
UID: NN:d3dcommon.ID3DInclude
title: ID3DInclude (d3dcommon.h)
description: ID3DInclude is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader
helpviewer_keywords: ["ID3DInclude","ID3DInclude interface [Direct3D 11]","ID3DInclude interface [Direct3D 11]","described","d3dcommon/ID3DInclude","direct3d11.id3dinclude"]
old-location: direct3d11\id3dinclude.htm
tech.root: direct3d11
ms.assetid: 2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5
ms.date: 12/05/2018
ms.keywords: ID3DInclude, ID3DInclude interface [Direct3D 11], ID3DInclude interface [Direct3D 11],described, d3dcommon/ID3DInclude, direct3d11.id3dinclude
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3DInclude
 - d3dcommon/ID3DInclude
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3DInclude
---

# ID3DInclude interface


## -description

<b>ID3DInclude</b> is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader #include files.

## -inheritance

The <b>ID3DInclude</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DInclude</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To use this interface, create an interface that inherits from <b>ID3DInclude</b> and implement custom behavior for the methods.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-interfaces">Common Version Interfaces</a>
