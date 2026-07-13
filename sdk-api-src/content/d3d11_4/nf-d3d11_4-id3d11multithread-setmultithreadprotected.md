---
UID: NF:d3d11_4.ID3D11Multithread.SetMultithreadProtected
title: ID3D11Multithread::SetMultithreadProtected (d3d11_4.h)
description: Turns multithread protection on or off.
helpviewer_keywords: ["ID3D11Multithread interface [Direct3D 11]","SetMultithreadProtected method","ID3D11Multithread.SetMultithreadProtected","ID3D11Multithread::SetMultithreadProtected","SetMultithreadProtected","SetMultithreadProtected method [Direct3D 11]","SetMultithreadProtected method [Direct3D 11]","ID3D11Multithread interface","d3d11_4/ID3D11Multithread::SetMultithreadProtected","direct3d11.id3d11multithread_setmultithreadprotected"]
old-location: direct3d11\id3d11multithread_setmultithreadprotected.htm
tech.root: direct3d11
ms.assetid: E8BF9A25-CCEA-44F3-AE7C-376E5B672079
ms.date: 12/05/2018
ms.keywords: ID3D11Multithread interface [Direct3D 11],SetMultithreadProtected method, ID3D11Multithread.SetMultithreadProtected, ID3D11Multithread::SetMultithreadProtected, SetMultithreadProtected, SetMultithreadProtected method [Direct3D 11], SetMultithreadProtected method [Direct3D 11],ID3D11Multithread interface, d3d11_4/ID3D11Multithread::SetMultithreadProtected, direct3d11.id3d11multithread_setmultithreadprotected
req.header: d3d11_4.h
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
req.dll: D3d11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Multithread::SetMultithreadProtected
 - d3d11_4/ID3D11Multithread::SetMultithreadProtected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.dll
api_name:
 - ID3D11Multithread.SetMultithreadProtected
---

# ID3D11Multithread::SetMultithreadProtected


## -description

Turns multithread protection on or off.

## -parameters

### -param bMTProtect [in]

Type: <b>BOOL</b>

Set to true to turn multithread protection on, false to turn it off.

## -returns

Type: <b>BOOL</b>

True if multithread protection was already turned on prior to calling this method, false otherwise.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-getmultithreadprotected">GetMultithreadProtected</a>



<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread">ID3D11Multithread</a>