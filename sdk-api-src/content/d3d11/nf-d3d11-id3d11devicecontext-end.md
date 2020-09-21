---
UID: NF:d3d11.ID3D11DeviceContext.End
title: ID3D11DeviceContext::End (d3d11.h)
description: Mark the end of a series of commands.
helpviewer_keywords: ["End","End method [Direct3D 11]","End method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","End method","ID3D11DeviceContext.End","ID3D11DeviceContext::End","c700f203-34b8-01ee-d941-99cff256b5c2","d3d11/ID3D11DeviceContext::End","direct3d11.id3d11devicecontext_end"]
old-location: direct3d11\id3d11devicecontext_end.htm
tech.root: direct3d11
ms.assetid: 9b941abc-04a3-4dd7-b72d-62cd5bd06b47
ms.date: 12/05/2018
ms.keywords: End, End method [Direct3D 11], End method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],End method, ID3D11DeviceContext.End, ID3D11DeviceContext::End, c700f203-34b8-01ee-d941-99cff256b5c2, d3d11/ID3D11DeviceContext::End, direct3d11.id3d11devicecontext_end
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
 - ID3D11DeviceContext::End
 - d3d11/ID3D11DeviceContext::End
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
 - ID3D11DeviceContext.End
---

# ID3D11DeviceContext::End


## -description

Mark the end of a series of commands.

## -parameters

### -param pAsync [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a> interface.

## -remarks

Use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> to mark the beginning of the series of commands.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>