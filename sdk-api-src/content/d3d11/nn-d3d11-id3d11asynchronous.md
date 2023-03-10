---
UID: NN:d3d11.ID3D11Asynchronous
title: ID3D11Asynchronous (d3d11.h)
description: This interface encapsulates methods for retrieving data from the GPU asynchronously. (ID3D11Asynchronous)
helpviewer_keywords: ["ID3D11Asynchronous","ID3D11Asynchronous interface [Direct3D 11]","ID3D11Asynchronous interface [Direct3D 11]","described","ba273b1e-153b-fd26-ff4e-e9755f4ea1f2","d3d11/ID3D11Asynchronous","direct3d11.id3d11asynchronous"]
old-location: direct3d11\id3d11asynchronous.htm
tech.root: direct3d11
ms.assetid: 37ff9dc0-5ec2-4cd5-b252-44e2dac45355
ms.date: 12/05/2018
ms.keywords: ID3D11Asynchronous, ID3D11Asynchronous interface [Direct3D 11], ID3D11Asynchronous interface [Direct3D 11],described, ba273b1e-153b-fd26-ff4e-e9755f4ea1f2, d3d11/ID3D11Asynchronous, direct3d11.id3d11asynchronous
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
 - ID3D11Asynchronous
 - d3d11/ID3D11Asynchronous
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
 - ID3D11Asynchronous
---

# ID3D11Asynchronous interface


## -description

This interface encapsulates methods for retrieving data from the GPU asynchronously.

## -inheritance

The <b>ID3D11Asynchronous</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11Asynchronous</b> also has these types of members:

## -remarks

There are three types of asynchronous interfaces, all of which inherit this interface:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11query">ID3D11Query</a> - Queries information from the GPU.</li>
<li>
<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a> - Determines whether a piece of geometry should be processed or not depending on the results of a previous draw call.</li>
<li>
<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11counter">ID3D11Counter</a> - Measures GPU performance.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
