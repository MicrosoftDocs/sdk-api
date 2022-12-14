---
UID: NN:d3d11.ID3D11Counter
title: ID3D11Counter (d3d11.h)
description: This interface encapsulates methods for measuring GPU performance. (ID3D11Counter)
helpviewer_keywords: ["ID3D11Counter","ID3D11Counter interface [Direct3D 11]","ID3D11Counter interface [Direct3D 11]","described","d3d11/ID3D11Counter","direct3d11.id3d11counter","e8e19b70-2584-4e44-1faf-1bc2d275606a"]
old-location: direct3d11\id3d11counter.htm
tech.root: direct3d11
ms.assetid: 3f35b3d5-f829-443c-9ea6-6cffdd4f58b7
ms.date: 12/05/2018
ms.keywords: ID3D11Counter, ID3D11Counter interface [Direct3D 11], ID3D11Counter interface [Direct3D 11],described, d3d11/ID3D11Counter, direct3d11.id3d11counter, e8e19b70-2584-4e44-1faf-1bc2d275606a
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
 - ID3D11Counter
 - d3d11/ID3D11Counter
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
 - ID3D11Counter
---

# ID3D11Counter interface


## -description

This interface encapsulates methods for measuring GPU performance.

## -inheritance

The <b>ID3D11Counter</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>. <b>ID3D11Counter</b> also has these types of members:

## -remarks

A counter can be created with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createcounter">ID3D11Device::CreateCounter</a>.

This is a derived class of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>.

Counter data is gathered by issuing an <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> command, and then calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_counter">D3D11_COUNTER</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>
