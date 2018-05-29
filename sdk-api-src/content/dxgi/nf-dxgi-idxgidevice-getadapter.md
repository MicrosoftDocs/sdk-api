---
UID: NF:dxgi.IDXGIDevice.GetAdapter
title: IDXGIDevice::GetAdapter
author: windows-sdk-content
description: Returns the adapter for the specified device.
old-location: direct3ddxgi\idxgidevice_getadapter.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_getadapter.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: 3bbfc03f-4bda-05eb-f6de-6f2c4564fa75, GetAdapter, GetAdapter method [DXGI], GetAdapter method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],GetAdapter method, IDXGIDevice.GetAdapter, IDXGIDevice::GetAdapter, direct3ddxgi.idxgidevice_getadapter, dxgi/IDXGIDevice::GetAdapter
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIDevice.GetAdapter
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

Type: <b><a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>**</b>

The address of an <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> interface pointer to the adapter.  This parameter must not be <b>NULL</b>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> that indicates failure. If the <i>pAdapter</i> parameter is <b>NULL</b> this method returns E_INVALIDARG.




## -remarks



If the <b>GetAdapter</b> method succeeds, the reference count on the adapter interface will be incremented. To avoid a memory leak, be sure to release the interface when you are finished using it.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>
 

 

