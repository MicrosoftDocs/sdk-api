---
UID: NN:dxgi.IDXGIAdapter
title: IDXGIAdapter
author: windows-sdk-content
description: The IDXGIAdapter interface represents a display subsystem (including one or more GPUs, DACs and video memory).
old-location: direct3ddxgi\idxgiadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 5f145307-fa6f-0182-45d3-5fa9da029cf2, IDXGIAdapter, IDXGIAdapter interface [DXGI], IDXGIAdapter interface [DXGI],described, direct3ddxgi.idxgiadapter, dxgi/IDXGIAdapter
ms.prod: windows
ms.technology: windows-sdk
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174541(v=VS.85).aspx">IDXGIObject</a>. <b>IDXGIAdapter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb174524(v=VS.85).aspx">CheckInterfaceSupport</a>
</td>
<td align="left" width="63%">
Checks whether the system supports a device interface for a graphics component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174525(v=VS.85).aspx">EnumOutputs</a>
</td>
<td align="left" width="63%">
Enumerate adapter (video card) outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174526(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.0 description of an adapter (or video card).

</td>
</tr>
</table> 


## -remarks



A display subsystem is often referred to as a video card, however, on some machines the display subsystem is part of the motherboard.
          

To enumerate the display subsystems, use <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">IDXGIFactory::EnumAdapters</a>.
          

To get an interface to the adapter for a particular device, use <a href="https://msdn.microsoft.com/en-us/library/Bb174531(v=VS.85).aspx">IDXGIDevice::GetAdapter</a>.
          

To create a software adapter, use <a href="https://msdn.microsoft.com/en-us/library/Bb174536(v=VS.85).aspx">IDXGIFactory::CreateSoftwareAdapter</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174541(v=VS.85).aspx">IDXGIObject</a>
 

 

