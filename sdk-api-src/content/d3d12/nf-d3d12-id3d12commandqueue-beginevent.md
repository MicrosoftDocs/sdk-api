---
UID: NF:d3d12.ID3D12CommandQueue.BeginEvent
title: ID3D12CommandQueue::BeginEvent
author: windows-sdk-content
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue.
old-location: direct3d12\id3d12commandqueue_beginevent.htm
old-project: direct3d12
ms.assetid: 09586D24-6D52-49BA-B6C0-793219FAE80C
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: BeginEvent, BeginEvent method, BeginEvent method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,BeginEvent method, ID3D12CommandQueue.BeginEvent, ID3D12CommandQueue::BeginEvent, d3d12/ID3D12CommandQueue::BeginEvent, direct3d12.id3d12commandqueue_beginevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ID3D12CommandQueue.BeginEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12CommandQueue::BeginEvent


## -description



          Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.


## -parameters




### -param Metadata

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Internal.


### -param pData [in, optional]

Type: <b>const void*</b>


            
            Internal.


### -param Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Internal.


## -returns




            This method does not return a value.
          




## -remarks



This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To mark the start of an instrumentation region at the current location within a D3D12 command queue, use the <b>PIXBeginEvent</b> function or <b>PIXScopedEvent</b> macro.  These are provided by the <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>
 

 

