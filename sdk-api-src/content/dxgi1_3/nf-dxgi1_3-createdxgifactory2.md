---
UID: NF:dxgi1_3.CreateDXGIFactory2
title: CreateDXGIFactory2 function
author: windows-sdk-content
description: Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.
old-location: direct3ddxgi\createdxgifactory2.htm
tech.root: direct3ddxgi
ms.assetid: D3CF43B0-8F17-486E-8750-CF0B9052BE74
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CreateDXGIFactory2, CreateDXGIFactory2 function [DXGI], direct3ddxgi.createdxgifactory2, dxgi1_3/CreateDXGIFactory2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxgi.dll
api_name:
 - CreateDXGIFactory2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateDXGIFactory2
: 
---

# CreateDXGIFactory2 function


## -description


Creates a DXGI 1.3 factory that you can use to generate other  DXGI objects.

In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it. Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead. Use <b>CreateDXGIFactory2</b> and specify the DXGI_CREATE_FACTORY_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.


## -parameters




### -param Flags

Type: <b>UINT</b>

Valid values include the <b>DXGI_CREATE_FACTORY_DEBUG (0x01)</b> flag, and zero.

<div class="alert"><b>Note</b>  This flag will be set by the D3D runtime if:<ul>
<li>The system creates an implicit factory during device creation.</li>
<li>The D3D11_CREATE_DEVICE_DEBUG flag is specified during device creation, for example using <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a> (or the swapchain method, or the Direct3D 10 equivalents).</li>
</ul>
</div>
<div> </div>

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a> object referenced by 
          the <i>ppFactory</i> parameter.


### -param ppFactory [out]

Type: <b>void**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



This function accepts a flag indicating whether DXGIDebug.dll is loaded. The function otherwise behaves identically to <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a>.




## -see-also




<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>
 

 

