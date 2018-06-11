---
UID: NF:dxgi.IDXGIDevice.GetGPUThreadPriority
title: IDXGIDevice::GetGPUThreadPriority
author: windows-sdk-content
description: Gets the GPU thread priority.
old-location: direct3ddxgi\idxgidevice_getgputhreadpriority.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_getgputhreadpriority.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetGPUThreadPriority, GetGPUThreadPriority method [DXGI], GetGPUThreadPriority method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],GetGPUThreadPriority method, IDXGIDevice.GetGPUThreadPriority, IDXGIDevice::GetGPUThreadPriority, direct3ddxgi.idxgidevice_getgputhreadpriority, dxgi/IDXGIDevice::GetGPUThreadPriority, fbea5e3b-9023-68ed-7a86-b421d1d2cf36
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
 - IDXGIDevice.GetGPUThreadPriority
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice::GetGPUThreadPriority


## -description


Gets the GPU thread priority.


## -parameters




### -param pPriority [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a>*</b>

A pointer to a variable that receives a value that indicates the current GPU thread priority. The value will be between -7 and 7, inclusive, where 0 represents normal priority.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Return S_OK if successful; otherwise, returns E_POINTER if the <i>pPriority</i> parameter is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>
 

 

