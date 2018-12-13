---
UID: NN:dxgi.IDXGIAdapter
title: IDXGIAdapter
author: windows-sdk-content
description: The IDXGIAdapter interface represents a display subsystem (including one or more GPUs, DACs and video memory).
old-location: direct3ddxgi\idxgiadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5f145307-fa6f-0182-45d3-5fa9da029cf2, IDXGIAdapter, IDXGIAdapter interface [DXGI], IDXGIAdapter interface [DXGI],described, direct3ddxgi.idxgiadapter, dxgi/IDXGIAdapter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IDXGIAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter interface


## -description


The <b>IDXGIAdapter</b> interface represents a display subsystem (including one or more GPUs, DACs and video memory).
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter</b> interface inherits from <a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>. <b>IDXGIAdapter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ed2f928-8442-4699-80e9-80393db5dd34">CheckInterfaceSupport</a>
</td>
<td align="left" width="63%">
Checks whether the system supports a device interface for a graphics component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29a826bb-6282-41d1-abf9-642ccb127774">EnumOutputs</a>
</td>
<td align="left" width="63%">
Enumerate adapter (video card) outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81d0cdaa-073e-4af8-b037-e61f1d5aa6fa">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.0 description of an adapter (or video card).

</td>
</tr>
</table> 


## -remarks



A display subsystem is often referred to as a video card, however, on some machines the display subsystem is part of the motherboard.
          

To enumerate the display subsystems, use <a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">IDXGIFactory::EnumAdapters</a>.
          

To get an interface to the adapter for a particular device, use <a href="https://msdn.microsoft.com/ae113b36-47fd-4db1-b10c-ced22ec52435">IDXGIDevice::GetAdapter</a>.
          

To create a software adapter, use <a href="https://msdn.microsoft.com/46c10086-aa57-42f6-a619-8c537e4ae406">IDXGIFactory::CreateSoftwareAdapter</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

