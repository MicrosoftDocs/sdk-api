---
UID: NF:d3d10.ID3D10Multithread.Leave
title: ID3D10Multithread::Leave (d3d10.h)
description: Leave a device's critical section. (ID3D10Multithread.Leave)
helpviewer_keywords: ["ID3D10Multithread interface [Direct3D 10]","Leave method","ID3D10Multithread.Leave","ID3D10Multithread::Leave","Leave","Leave method [Direct3D 10]","Leave method [Direct3D 10]","ID3D10Multithread interface","d3d10/ID3D10Multithread::Leave","direct3d10.id3d10multithread_leave","f69302dd-2d93-2366-c5f5-206d6140c16e"]
old-location: direct3d10\id3d10multithread_leave.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_leave.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Multithread interface [Direct3D 10],Leave method, ID3D10Multithread.Leave, ID3D10Multithread::Leave, Leave, Leave method [Direct3D 10], Leave method [Direct3D 10],ID3D10Multithread interface, d3d10/ID3D10Multithread::Leave, direct3d10.id3d10multithread_leave, f69302dd-2d93-2366-c5f5-206d6140c16e
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
 - ID3D10Multithread::Leave
 - d3d10/ID3D10Multithread::Leave
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
 - ID3D10Multithread.Leave
---

# ID3D10Multithread::Leave


## -description

Leave a device's critical section.



## -remarks

This function is typically used in multithreaded applications when there is a series of graphics commands that must happen in order. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10multithread-enter">ID3D10Multithread::Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically called after those graphics commands.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread</a>
