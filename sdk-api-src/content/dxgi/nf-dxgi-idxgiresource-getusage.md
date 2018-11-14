---
UID: NF:dxgi.IDXGIResource.GetUsage
title: IDXGIResource::GetUsage
author: windows-sdk-content
description: Get the expected resource usage.
old-location: direct3ddxgi\idxgiresource_getusage.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_getusage.htm
ms.author: windowssdkdev
ms.date: 11/13/2018
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
 - IDXGIResource.GetUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi.h
: 
- IDXGIResource.GetUsage
: 
---

# IDXGIResource::GetUsage


## -description


Get the expected resource usage.


## -parameters




### -param pUsage

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173078(v=VS.85).aspx">DXGI_USAGE</a>*</b>

A pointer to a usage flag (see <a href="https://msdn.microsoft.com/en-us/library/Bb173078(v=VS.85).aspx">DXGI_USAGE</a>). For Direct3D 10, a surface can be used as a shader input or a render-target output.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174560(v=VS.85).aspx">IDXGIResource</a>
 

 

