---
UID: NN:dxgi.IDXGIAdapter
title: IDXGIAdapter (dxgi.h)
author: windows-sdk-content
description: The IDXGIAdapter interface represents a display subsystem (including one or more GPUs, DACs and video memory).
old-location: direct3ddxgi\idxgiadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiadapter.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5f145307-fa6f-0182-45d3-5fa9da029cf2, IDXGIAdapter, IDXGIAdapter interface [DXGI], IDXGIAdapter interface [DXGI],described, direct3ddxgi.idxgiadapter, dxgi/IDXGIAdapter
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
ms.custom: 19H1
---

# IDXGIAdapter interface


## -description


The <b>IDXGIAdapter</b> interface represents a display subsystem (including one or more GPUs, DACs and video memory).
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIAdapter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-checkinterfacesupport">CheckInterfaceSupport</a>
</td>
<td align="left" width="63%">
Checks whether the system supports a device interface for a graphics component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">EnumOutputs</a>
</td>
<td align="left" width="63%">
Enumerate adapter (video card) outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.0 description of an adapter (or video card).

</td>
</tr>
</table> 


## -remarks



A display subsystem is often referred to as a video card, however, on some machines the display subsystem is part of the motherboard.
          

To enumerate the display subsystems, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory::EnumAdapters</a>.
          

To get an interface to the adapter for a particular device, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter">IDXGIDevice::GetAdapter</a>.
          

To create a software adapter, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createsoftwareadapter">IDXGIFactory::CreateSoftwareAdapter</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
 

 

