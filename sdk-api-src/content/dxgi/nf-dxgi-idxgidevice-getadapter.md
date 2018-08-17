---
UID: NF:dxgi.IDXGIDevice.GetAdapter
title: IDXGIDevice::GetAdapter
author: windows-sdk-content
description: Returns the adapter for the specified device.
old-location: direct3ddxgi\idxgidevice_getadapter.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_getadapter.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 3bbfc03f-4bda-05eb-f6de-6f2c4564fa75, GetAdapter, GetAdapter method [DXGI], GetAdapter method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],GetAdapter method, IDXGIDevice.GetAdapter, IDXGIDevice::GetAdapter, direct3ddxgi.idxgidevice_getadapter, dxgi/IDXGIDevice::GetAdapter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
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
 - IDXGIDevice.GetAdapter
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice::GetAdapter


## -description


Returns the adapter for the specified device.


## -parameters




### -param pAdapter [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>**</b>

The address of an <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> interface pointer to the adapter.  This parameter must not be <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> that indicates failure. If the <i>pAdapter</i> parameter is <b>NULL</b> this method returns E_INVALIDARG.




## -remarks



If the <b>GetAdapter</b> method succeeds, the reference count on the adapter interface will be incremented. To avoid a memory leak, be sure to release the interface when you are finished using it.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>
 

 

