---
UID: NF:dxgi.IDXGIResource.GetUsage
title: IDXGIResource::GetUsage
author: windows-driver-content
description: Get the expected resource usage.
old-location: direct3ddxgi\idxgiresource_getusage.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_getusage.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: 1fc82eef-f409-1d78-ab65-dd0124809d16, GetUsage, GetUsage method [DXGI], GetUsage method [DXGI],IDXGIResource interface, IDXGIResource interface [DXGI],GetUsage method, IDXGIResource.GetUsage, IDXGIResource::GetUsage, direct3ddxgi.idxgiresource_getusage, dxgi/IDXGIResource::GetUsage
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IDXGIResource.GetUsage
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIResource::GetUsage


## -description


Get the expected resource usage.


## -parameters




### -param pUsage

Type: <b><a href="https://msdn.microsoft.com/b5026566-89b5-458e-b36d-a55e5f8c10c1">DXGI_USAGE</a>*</b>

A pointer to a usage flag (see <a href="https://msdn.microsoft.com/b5026566-89b5-458e-b36d-a55e5f8c10c1">DXGI_USAGE</a>). For Direct3D 10, a surface can be used as a shader input or a render-target output.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a>
 

 

