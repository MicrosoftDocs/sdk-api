---
UID: NF:dxgi.IDXGIDevice1.SetMaximumFrameLatency
title: IDXGIDevice1::SetMaximumFrameLatency
author: windows-sdk-content
description: Sets the number of frames that the system is allowed to queue for rendering.
old-location: direct3ddxgi\idxgidevice1_setmaximumframelatency.htm
old-project: direct3ddxgi
ms.assetid: ea477f33-2dba-44ac-9b47-8fd2ce6cec30
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDXGIDevice1 interface [DXGI],SetMaximumFrameLatency method, IDXGIDevice1.SetMaximumFrameLatency, IDXGIDevice1::SetMaximumFrameLatency, SetMaximumFrameLatency, SetMaximumFrameLatency method [DXGI], SetMaximumFrameLatency method [DXGI],IDXGIDevice1 interface, da92b152-07cc-06ca-caa5-a8982fe8fc2f, direct3ddxgi.idxgidevice1_setmaximumframelatency, dxgi/IDXGIDevice1::SetMaximumFrameLatency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice1.SetMaximumFrameLatency
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice1::SetMaximumFrameLatency


## -description


Sets the number of frames that the system is allowed to queue for rendering.


## -parameters




### -param MaxLatency

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of back buffer frames that a driver can queue. The value defaults to 3, but 
      can range from 1 to 16. A value of 0 will reset latency to the default.  For multi-head devices, this value is specified per-head.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, DXGI_ERROR_DEVICE_REMOVED if the device was removed.




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

Frame latency is the number of frames that are allowed to be stored in a queue before submission for rendering.  Latency is often used to 
    control how the CPU chooses between responding to user input and frames that are in the render queue.  It is often beneficial for applications that 
    have no user input (for example, video playback) to queue more than 3 frames of data.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>



<a href="https://msdn.microsoft.com/87b98c47-3556-4588-97b2-c935d7052286">IDXGIDevice1::GetMaximumFrameLatency</a>
 

 

