---
UID: NF:d3d12.ID3D12CommandQueue.EndEvent
title: ID3D12CommandQueue::EndEvent (d3d12.h)
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue. (ID3D12CommandQueue.EndEvent)
helpviewer_keywords: ["EndEvent","EndEvent method","EndEvent method","ID3D12CommandQueue interface","ID3D12CommandQueue interface","EndEvent method","ID3D12CommandQueue.EndEvent","ID3D12CommandQueue::EndEvent","d3d12/ID3D12CommandQueue::EndEvent","direct3d12.id3d12commandqueue_endevent"]
old-location: direct3d12\id3d12commandqueue_endevent.htm
tech.root: direct3d12
ms.assetid: CA45061A-3DD6-4FFB-9723-ED33343052F3
ms.date: 12/05/2018
ms.keywords: EndEvent, EndEvent method, EndEvent method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,EndEvent method, ID3D12CommandQueue.EndEvent, ID3D12CommandQueue::EndEvent, d3d12/ID3D12CommandQueue::EndEvent, direct3d12.id3d12commandqueue_endevent
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12CommandQueue::EndEvent
 - d3d12/ID3D12CommandQueue::EndEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.EndEvent
---

# ID3D12CommandQueue::EndEvent


## -description

Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.



## -remarks

This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To mark the end of an instrumentation region at the current location within a D3D12 command queue, use the <b>PIXEndEvent</b> function or <b>PIXScopedEvent</b> macro.  These are provided by the <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>
