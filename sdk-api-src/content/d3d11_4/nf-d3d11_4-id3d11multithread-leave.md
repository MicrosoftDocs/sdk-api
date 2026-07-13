---
UID: NF:d3d11_4.ID3D11Multithread.Leave
title: ID3D11Multithread::Leave (d3d11_4.h)
description: Leave a device's critical section. (ID3D11Multithread.Leave)
helpviewer_keywords: ["ID3D11Multithread interface [Direct3D 11]","Leave method","ID3D11Multithread.Leave","ID3D11Multithread::Leave","Leave","Leave method [Direct3D 11]","Leave method [Direct3D 11]","ID3D11Multithread interface","d3d11_4/ID3D11Multithread::Leave","direct3d11.id3d11multithread_leave"]
old-location: direct3d11\id3d11multithread_leave.htm
tech.root: direct3d11
ms.assetid: CECBE440-3F9E-4649-B257-BAD3E7F5CF2F
ms.date: 12/05/2018
ms.keywords: ID3D11Multithread interface [Direct3D 11],Leave method, ID3D11Multithread.Leave, ID3D11Multithread::Leave, Leave, Leave method [Direct3D 11], Leave method [Direct3D 11],ID3D11Multithread interface, d3d11_4/ID3D11Multithread::Leave, direct3d11.id3d11multithread_leave
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
 - ID3D11Multithread::Leave
 - d3d11_4/ID3D11Multithread::Leave
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
 - ID3D11Multithread.Leave
---

# ID3D11Multithread::Leave


## -description

Leave a device's critical section.



## -remarks

This function is typically used in multithreaded applications when there is a series of graphics commands 
		  that must happen in order. <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-enter">Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically 
		  called after those graphics commands.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread">ID3D11Multithread</a>
