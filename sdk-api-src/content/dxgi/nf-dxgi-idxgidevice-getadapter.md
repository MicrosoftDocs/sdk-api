---
UID: NF:dxgi.IDXGIDevice.GetAdapter
title: IDXGIDevice::GetAdapter (dxgi.h)
author: windows-sdk-content
description: Returns the adapter for the specified device.
old-location: direct3ddxgi\idxgidevice_getadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_getadapter.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3bbfc03f-4bda-05eb-f6de-6f2c4564fa75, GetAdapter, GetAdapter method [DXGI], GetAdapter method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],GetAdapter method, IDXGIDevice.GetAdapter, IDXGIDevice::GetAdapter, direct3ddxgi.idxgidevice_getadapter, dxgi/IDXGIDevice::GetAdapter
ms.topic: method
f1_keywords: 
 - "dxgi/IDXGIDevice.GetAdapter"
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
 - IDXGIDevice.GetAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDevice::GetAdapter


## -description


Returns the adapter for the specified device.


## -parameters




### -param pAdapter [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>**</b>

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> interface pointer to the adapter.  This parameter must not be <b>NULL</b>.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> that indicates failure. If the <i>pAdapter</i> parameter is <b>NULL</b> this method returns E_INVALIDARG.




## -remarks



If the <b>GetAdapter</b> method succeeds, the reference count on the adapter interface will be incremented. To avoid a memory leak, be sure to release the interface when you are finished using it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>
 

 

