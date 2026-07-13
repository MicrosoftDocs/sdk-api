---
UID: NF:d3d11_4.ID3D11Multithread.Enter
title: ID3D11Multithread::Enter (d3d11_4.h)
description: Enter a device's critical section. (ID3D11Multithread.Enter)
helpviewer_keywords: ["Enter","Enter method [Direct3D 11]","Enter method [Direct3D 11]","ID3D11Multithread interface","ID3D11Multithread interface [Direct3D 11]","Enter method","ID3D11Multithread.Enter","ID3D11Multithread::Enter","d3d11_4/ID3D11Multithread::Enter","direct3d11.id3d11multithread_enter"]
old-location: direct3d11\id3d11multithread_enter.htm
tech.root: direct3d11
ms.assetid: A742D03A-0A47-4B08-952A-836A272D1519
ms.date: 12/05/2018
ms.keywords: Enter, Enter method [Direct3D 11], Enter method [Direct3D 11],ID3D11Multithread interface, ID3D11Multithread interface [Direct3D 11],Enter method, ID3D11Multithread.Enter, ID3D11Multithread::Enter, d3d11_4/ID3D11Multithread::Enter, direct3d11.id3d11multithread_enter
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
 - ID3D11Multithread::Enter
 - d3d11_4/ID3D11Multithread::Enter
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
 - ID3D11Multithread.Enter
---

# ID3D11Multithread::Enter


## -description

Enter a device's critical section.



## -remarks

If <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-setmultithreadprotected">SetMultithreadProtected</a> is set to true, then entering a device's critical section prevents other threads from simultaneously calling that device's methods, calling DXGI methods, and calling the methods of all resource, view, shader, state, and asynchronous interfaces.

This function should be used in multithreaded applications when there is a series of graphics commands that must happen in order. This function is typically called at the beginning of the series of graphics commands, and <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-leave">Leave</a> is typically called after those graphics commands.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread">ID3D11Multithread</a>
