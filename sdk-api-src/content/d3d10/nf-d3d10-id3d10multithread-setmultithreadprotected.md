---
UID: NF:d3d10.ID3D10Multithread.SetMultithreadProtected
title: ID3D10Multithread::SetMultithreadProtected (d3d10.h)
description: Turn multithreading on or off.
helpviewer_keywords: ["22302703-e7e4-5872-896b-8c2360171b16","ID3D10Multithread interface [Direct3D 10]","SetMultithreadProtected method","ID3D10Multithread.SetMultithreadProtected","ID3D10Multithread::SetMultithreadProtected","SetMultithreadProtected","SetMultithreadProtected method [Direct3D 10]","SetMultithreadProtected method [Direct3D 10]","ID3D10Multithread interface","d3d10/ID3D10Multithread::SetMultithreadProtected","direct3d10.id3d10multithread_setmultithreadprotected"]
old-location: direct3d10\id3d10multithread_setmultithreadprotected.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_setmultithreadprotected.htm
ms.date: 12/05/2018
ms.keywords: 22302703-e7e4-5872-896b-8c2360171b16, ID3D10Multithread interface [Direct3D 10],SetMultithreadProtected method, ID3D10Multithread.SetMultithreadProtected, ID3D10Multithread::SetMultithreadProtected, SetMultithreadProtected, SetMultithreadProtected method [Direct3D 10], SetMultithreadProtected method [Direct3D 10],ID3D10Multithread interface, d3d10/ID3D10Multithread::SetMultithreadProtected, direct3d10.id3d10multithread_setmultithreadprotected
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
 - ID3D10Multithread::SetMultithreadProtected
 - d3d10/ID3D10Multithread::SetMultithreadProtected
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
 - ID3D10Multithread.SetMultithreadProtected
---

# ID3D10Multithread::SetMultithreadProtected


## -description

Turn multithreading on or off.

## -parameters

### -param bMTProtect [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

True to turn multithreading on, false to turn it off.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

True if multithreading was turned on prior to calling this method, false otherwise.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread Interface</a>