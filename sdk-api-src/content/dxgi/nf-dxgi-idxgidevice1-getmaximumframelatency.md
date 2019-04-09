---
UID: NF:dxgi.IDXGIDevice1.GetMaximumFrameLatency
title: IDXGIDevice1::GetMaximumFrameLatency (dxgi.h)
author: windows-sdk-content
description: Gets the number of frames that the system is allowed to queue for rendering.
old-location: direct3ddxgi\idxgidevice1_getmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: 87b98c47-3556-4588-97b2-c935d7052286
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 65e01dd1-b488-81d7-8806-77a7e4bb8f02, GetMaximumFrameLatency, GetMaximumFrameLatency method [DXGI], GetMaximumFrameLatency method [DXGI],IDXGIDevice1 interface, IDXGIDevice1 interface [DXGI],GetMaximumFrameLatency method, IDXGIDevice1.GetMaximumFrameLatency, IDXGIDevice1::GetMaximumFrameLatency, direct3ddxgi.idxgidevice1_getmaximumframelatency, dxgi/IDXGIDevice1::GetMaximumFrameLatency
ms.topic: method
req.header: dxgi.h
req.include-header: 
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice1.GetMaximumFrameLatency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDevice1::GetMaximumFrameLatency


## -description


Gets the number of frames that the system is allowed to queue for rendering.


## -parameters




### -param pMaxLatency [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

This value is set to the number of frames that can be queued for render.  
      This value defaults to 3, but can range from 1 to 16.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following members of the <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a> enumerated type:

<ul>
<li><b>D3DERR_DEVICELOST</b></li>
<li><b>D3DERR_DEVICEREMOVED</b></li>
<li><b>D3DERR_DRIVERINTERNALERROR</b></li>
<li><b>D3DERR_INVALIDCALL</b></li>
<li><b>D3DERR_OUTOFVIDEOMEMORY</b></li>
</ul>



## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

Frame latency is the number of frames that are allowed to be stored in a queue before submission for rendering.  Latency is often 
    used to control how the CPU chooses between responding to user input and frames that are in the render queue.  It is often beneficial for applications 
    that have no user input (for example, video playback) to queue more than 3 frames of data.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>



<a href="https://msdn.microsoft.com/ea477f33-2dba-44ac-9b47-8fd2ce6cec30">IDXGIDevice1::SetMaximumFrameLatency</a>
 

 

