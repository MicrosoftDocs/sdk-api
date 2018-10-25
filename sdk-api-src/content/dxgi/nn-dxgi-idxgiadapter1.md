---
UID: NN:dxgi.IDXGIAdapter1
title: IDXGIAdapter1
author: windows-sdk-content
description: The IDXGIAdapter1 interface represents a display sub-system (including one or more GPU's, DACs and video memory).
old-location: direct3ddxgi\idxgiadapter1.htm
tech.root: direct3ddxgi
ms.assetid: 003d5a10-e978-481f-8ca6-9e5ab69bfec0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 2ac7b82f-b5a5-ec94-1506-33b758455dd2, IDXGIAdapter1, IDXGIAdapter1 interface [DXGI], IDXGIAdapter1 interface [DXGI],described, direct3ddxgi.idxgiadapter1, dxgi/IDXGIAdapter1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IDXGIAdapter1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter1 interface


## -description


The <b>IDXGIAdapter1</b> interface represents a display sub-system (including one or more GPU's, DACs and video memory).
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter1</b> interface inherits from <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>. <b>IDXGIAdapter1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eb051f8-4e64-41fe-8177-6aad47714cb9">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a DXGI 1.1 description of an adapter (or video card).

</td>
</tr>
</table> 


## -remarks



This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on
            Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).
          

A display sub-system is often referred to as a video card, however, on some machines the display sub-system is part of the mother board.

To enumerate the display sub-systems, use <a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">IDXGIFactory1::EnumAdapters1</a>. To get an interface to the adapter for a
            particular device, use <a href="https://msdn.microsoft.com/ae113b36-47fd-4db1-b10c-ced22ec52435">IDXGIDevice::GetAdapter</a>. To create a software adapter, use <a href="https://msdn.microsoft.com/46c10086-aa57-42f6-a619-8c537e4ae406">IDXGIFactory::CreateSoftwareAdapter</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>
 

 

