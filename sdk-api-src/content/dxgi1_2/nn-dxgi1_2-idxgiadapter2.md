---
UID: NN:dxgi1_2.IDXGIAdapter2
title: IDXGIAdapter2 (dxgi1_2.h)
description: The IDXGIAdapter2 interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory.helpviewer_keywords: ["IDXGIAdapter2","IDXGIAdapter2 interface [DXGI]","IDXGIAdapter2 interface [DXGI]","described","direct3ddxgi.idxgiadapter2","dxgi1_2/IDXGIAdapter2"]
old-location: direct3ddxgi\idxgiadapter2.htm
tech.root: direct3ddxgi
ms.assetid: 9AAD133C-CE40-498B-827F-2B35C7C15B8C
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter2, IDXGIAdapter2 interface [DXGI], IDXGIAdapter2 interface [DXGI],described, direct3ddxgi.idxgiadapter2, dxgi1_2/IDXGIAdapter2
f1_keywords:
- dxgi1_2/IDXGIAdapter2
dev_langs:
- c++
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dxgi.lib
- Dxgi.dll
api_name:
- IDXGIAdapter2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIAdapter2 interface


## -description


The <b>IDXGIAdapter2</b> interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>. <b>IDXGIAdapter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiadapter2-getdesc2">GetDesc2</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.2 description of an adapter or video card. This description includes information about the granularity at which the GPU can be preempted from performing its current task.

</td>
</tr>
</table> 


## -remarks



A display subsystem is often referred to as a video card; however, on some computers, the display subsystem is part of the motherboard.
        

To enumerate the display subsystems, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>.
        

To get an interface to the adapter for a particular device, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter">IDXGIDevice::GetAdapter</a>.
        

To create a software adapter, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createsoftwareadapter">IDXGIFactory::CreateSoftwareAdapter</a>.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>
 

 

