---
UID: NF:dxgi.IDXGIDevice.SetGPUThreadPriority
title: IDXGIDevice::SetGPUThreadPriority
author: windows-sdk-content
description: Sets the GPU thread priority.
old-location: direct3ddxgi\idxgidevice_setgputhreadpriority.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_setgputhreadpriority.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGIDevice interface [DXGI],SetGPUThreadPriority method, IDXGIDevice.SetGPUThreadPriority, IDXGIDevice::SetGPUThreadPriority, SetGPUThreadPriority, SetGPUThreadPriority method [DXGI], SetGPUThreadPriority method [DXGI],IDXGIDevice interface, b610ce23-f003-9031-4c67-b5013c5af229, direct3ddxgi.idxgidevice_setgputhreadpriority, dxgi/IDXGIDevice::SetGPUThreadPriority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
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
 - IDXGIDevice.SetGPUThreadPriority
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice::SetGPUThreadPriority


## -description


Sets the GPU thread priority.


## -parameters




### -param Priority

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value that specifies the required GPU thread priority. This value must be between -7 and 7, inclusive, where 0 represents normal priority.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Return S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Priority</i> parameter is invalid.




## -remarks



The values for the <i>Priority</i> parameter function as follows:

<ul>
<li>Positive values increase the likelihood that the GPU scheduler will grant GPU execution cycles to the device when rendering.</li>
<li>Negative values lessen the likelihood that the device will receive GPU execution cycles when devices compete for them.</li>
<li>The device is guaranteed to receive some GPU execution cycles at all settings.</li>
</ul>
To use the <b>SetGPUThreadPriority</b> method, you should have a comprehensive understanding of GPU scheduling. You should profile your application to ensure that it behaves as intended. If used inappropriately, the <b>SetGPUThreadPriority</b> method can impede rendering speed and result in a poor user experience.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>



<a href="https://msdn.microsoft.com/library/Bb174532(v=VS.85).aspx">IDXGIDevice::GetGPUThreadPriority</a>
 

 

