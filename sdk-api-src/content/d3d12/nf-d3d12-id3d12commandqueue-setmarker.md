---
UID: NF:d3d12.ID3D12CommandQueue.SetMarker
title: ID3D12CommandQueue::SetMarker
author: windows-sdk-content
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue.
old-location: direct3d12\id3d12commandqueue_setmarker.htm
tech.root: direct3d12
ms.assetid: 993996E9-40B8-4FC6-B1CF-883829F8D1F5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12CommandQueue interface,SetMarker method, ID3D12CommandQueue.SetMarker, ID3D12CommandQueue::SetMarker, SetMarker, SetMarker method, SetMarker method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::SetMarker, direct3d12.id3d12commandqueue_setmarker
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.SetMarker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandQueue::SetMarker


## -description


Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command queue.


## -parameters




### -param Metadata

Type: <b>UINT</b>

Internal.
          


### -param pData [in, optional]

Type: <b>const void*</b>

Internal.


### -param Size

Type: <b>UINT</b>

Internal.


## -returns



This method does not return a value.
          




## -remarks



This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To insert instrumentation markers at the current location within a D3D12 command queue, use the <b>PIXSetMarker</b> function.  This is provided by the <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>
 

 

