---
UID: NN:d3d10.ID3D10Asynchronous
title: ID3D10Asynchronous (d3d10.h)
description: This interface encapsulates methods for retrieving data from the GPU asynchronously. (ID3D10Asynchronous)
helpviewer_keywords: ["ID3D10Asynchronous","ID3D10Asynchronous interface [Direct3D 10]","ID3D10Asynchronous interface [Direct3D 10]","described","bbcae8e9-6f10-e6ca-52e5-20302edce780","d3d10/ID3D10Asynchronous","direct3d10.id3d10asynchronous"]
old-location: direct3d10\id3d10asynchronous.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10asynchronous.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Asynchronous, ID3D10Asynchronous interface [Direct3D 10], ID3D10Asynchronous interface [Direct3D 10],described, bbcae8e9-6f10-e6ca-52e5-20302edce780, d3d10/ID3D10Asynchronous, direct3d10.id3d10asynchronous
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Asynchronous
 - d3d10/ID3D10Asynchronous
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Asynchronous
---

# ID3D10Asynchronous interface


## -description

This interface encapsulates methods for retrieving data from the GPU asynchronously.

## -inheritance

The <b>ID3D10Asynchronous</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10Asynchronous</b> also has these types of members:

## -remarks

There are three types of asynchronous interfaces, all of which inherit this interface:

<ul>
<li>
<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10query">ID3D10Query Interface</a> - Queries information from the GPU.</li>
<li>
<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate Interface</a> - Determines whether a piece of geometry should be processed or not depending on the results of a previous draw call.</li>
<li>
<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10counter">ID3D10Counter Interface</a> - Measures GPU performance.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
