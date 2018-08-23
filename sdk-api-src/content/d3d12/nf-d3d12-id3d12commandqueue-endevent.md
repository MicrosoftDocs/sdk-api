---
UID: NF:d3d12.ID3D12CommandQueue.EndEvent
title: ID3D12CommandQueue::EndEvent
author: windows-sdk-content
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue.
old-location: direct3d12\id3d12commandqueue_endevent.htm
old-project: direct3d12
ms.assetid: CA45061A-3DD6-4FFB-9723-ED33343052F3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: EndEvent, EndEvent method, EndEvent method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,EndEvent method, ID3D12CommandQueue.EndEvent, ID3D12CommandQueue::EndEvent, d3d12/ID3D12CommandQueue::EndEvent, direct3d12.id3d12commandqueue_endevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.EndEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12CommandQueue::EndEvent


## -description


Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.


## -parameters






## -returns



This method does not return a value.
          




## -remarks



This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To mark the end of an instrumentation region at the current location within a D3D12 command queue, use the <b>PIXEndEvent</b> function or <b>PIXScopedEvent</b> macro.  These are provided by the <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788627(v=VS.85).aspx">ID3D12CommandQueue</a>
 

 

