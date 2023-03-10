---
UID: NN:d3d10.ID3D10Counter
title: ID3D10Counter (d3d10.h)
description: This interface encapsulates methods for measuring GPU performance. (ID3D10Counter)
helpviewer_keywords: ["004d04e1-a54d-6c89-c551-db2d30d9d7e9","ID3D10Counter","ID3D10Counter interface [Direct3D 10]","ID3D10Counter interface [Direct3D 10]","described","d3d10/ID3D10Counter","direct3d10.id3d10counter"]
old-location: direct3d10\id3d10counter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10counter.htm
ms.date: 12/05/2018
ms.keywords: 004d04e1-a54d-6c89-c551-db2d30d9d7e9, ID3D10Counter, ID3D10Counter interface [Direct3D 10], ID3D10Counter interface [Direct3D 10],described, d3d10/ID3D10Counter, direct3d10.id3d10counter
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
 - ID3D10Counter
 - d3d10/ID3D10Counter
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
 - ID3D10Counter
---

# ID3D10Counter interface


## -description

This interface encapsulates methods for measuring GPU performance.

## -inheritance

The <b>ID3D10Counter</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous</a>. <b>ID3D10Counter</b> also has these types of members:

## -remarks

A counter can be created with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createcounter">ID3D10Device::CreateCounter</a>.

This is a derived class of <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous Interface</a>.

Counter data is gathered by issuing an <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">ID3D10Asynchronous::Begin</a> command, issuing some graphics commands, issuing an <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">ID3D10Asynchronous::End</a> command, and then calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_counter">D3D10_COUNTER</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10asynchronous">ID3D10Asynchronous</a>
