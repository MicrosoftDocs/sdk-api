---
UID: NF:d3d10.ID3D10Multithread.Enter
title: ID3D10Multithread::Enter (d3d10.h)
description: Enter a device's critical section. (ID3D10Multithread.Enter)
helpviewer_keywords: ["Enter","Enter method [Direct3D 10]","Enter method [Direct3D 10]","ID3D10Multithread interface","ID3D10Multithread interface [Direct3D 10]","Enter method","ID3D10Multithread.Enter","ID3D10Multithread::Enter","d34de96c-b476-19e4-cf57-4e43604474ab","d3d10/ID3D10Multithread::Enter","direct3d10.id3d10multithread_enter"]
old-location: direct3d10\id3d10multithread_enter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_enter.htm
ms.date: 12/05/2018
ms.keywords: Enter, Enter method [Direct3D 10], Enter method [Direct3D 10],ID3D10Multithread interface, ID3D10Multithread interface [Direct3D 10],Enter method, ID3D10Multithread.Enter, ID3D10Multithread::Enter, d34de96c-b476-19e4-cf57-4e43604474ab, d3d10/ID3D10Multithread::Enter, direct3d10.id3d10multithread_enter
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
 - ID3D10Multithread::Enter
 - d3d10/ID3D10Multithread::Enter
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
 - ID3D10Multithread.Enter
---

# ID3D10Multithread::Enter


## -description

Enter a device's critical section.



## -remarks

Entering a device's critical section prevents other threads from simultaneously calling that device's methods (if <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected">multithread protection</a> is set to true), calling DXGI methods, and calling the methods of all resource, view, shader, state, and asynchronous interfaces.

This function should be used in multithreaded applications when there is a series of graphics commands that must happen in order. This function is typically called at the beginning of the series of graphics commands, and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10multithread-leave">ID3D10Multithread::Leave</a> is typically called after those graphics commands.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread</a>
