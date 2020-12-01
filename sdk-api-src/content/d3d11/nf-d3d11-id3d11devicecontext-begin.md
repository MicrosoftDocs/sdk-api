---
UID: NF:d3d11.ID3D11DeviceContext.Begin
title: ID3D11DeviceContext::Begin (d3d11.h)
description: Mark the beginning of a series of commands.
helpviewer_keywords: ["Begin","Begin method [Direct3D 11]","Begin method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","Begin method","ID3D11DeviceContext.Begin","ID3D11DeviceContext::Begin","d3d11/ID3D11DeviceContext::Begin","direct3d11.id3d11devicecontext_begin","e0186f02-1f56-8ba4-2429-48dc47ff8dc9"]
old-location: direct3d11\id3d11devicecontext_begin.htm
tech.root: direct3d11
ms.assetid: 5a9cdc60-2226-4d18-bfbd-5db10de35e53
ms.date: 12/05/2018
ms.keywords: Begin, Begin method [Direct3D 11], Begin method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],Begin method, ID3D11DeviceContext.Begin, ID3D11DeviceContext::Begin, d3d11/ID3D11DeviceContext::Begin, direct3d11.id3d11devicecontext_begin, e0186f02-1f56-8ba4-2429-48dc47ff8dc9
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::Begin
 - d3d11/ID3D11DeviceContext::Begin
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
 - ID3D11DeviceContext.Begin
---

# ID3D11DeviceContext::Begin


## -description

Mark the beginning of a series of commands.

## -parameters

### -param pAsync [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a> interface.

## -remarks

Use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> to mark the ending of the series of commands.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>