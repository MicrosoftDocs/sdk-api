---
UID: NF:d3d11.ID3D11DeviceContext.GetContextFlags
title: ID3D11DeviceContext::GetContextFlags (d3d11.h)
description: Gets the initialization flags associated with the current deferred context.
helpviewer_keywords: ["6f9bf33e-cbe5-0def-cecd-cb59d7e3a8f4","GetContextFlags","GetContextFlags method [Direct3D 11]","GetContextFlags method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GetContextFlags method","ID3D11DeviceContext.GetContextFlags","ID3D11DeviceContext::GetContextFlags","d3d11/ID3D11DeviceContext::GetContextFlags","direct3d11.id3d11devicecontext_getcontextflags"]
old-location: direct3d11\id3d11devicecontext_getcontextflags.htm
tech.root: direct3d11
ms.assetid: 063fbcaf-2216-4090-a4cb-79091ed9b87a
ms.date: 12/05/2018
ms.keywords: 6f9bf33e-cbe5-0def-cecd-cb59d7e3a8f4, GetContextFlags, GetContextFlags method [Direct3D 11], GetContextFlags method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GetContextFlags method, ID3D11DeviceContext.GetContextFlags, ID3D11DeviceContext::GetContextFlags, d3d11/ID3D11DeviceContext::GetContextFlags, direct3d11.id3d11devicecontext_getcontextflags
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::GetContextFlags
 - d3d11/ID3D11DeviceContext::GetContextFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11DeviceContext.GetContextFlags
---

# ID3D11DeviceContext::GetContextFlags


## -description

Gets the initialization flags associated with the current deferred context.



## -remarks

The GetContextFlags method gets the flags that were supplied to the <i>ContextFlags</i> parameter of <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdeferredcontext">ID3D11Device::CreateDeferredContext</a>; however, the context flag is reserved for future use.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
