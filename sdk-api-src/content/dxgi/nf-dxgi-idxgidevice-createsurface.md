---
UID: NF:dxgi.IDXGIDevice.CreateSurface
title: IDXGIDevice::CreateSurface
author: windows-sdk-content
description: Returns a surface. This method is used internally and you should not call it directly in your application.
old-location: direct3ddxgi\idxgidevice_createsurface.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_createsurface.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CreateSurface, CreateSurface method [DXGI], CreateSurface method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],CreateSurface method, IDXGIDevice.CreateSurface, IDXGIDevice::CreateSurface, a6514b10-4398-2f19-86d3-e31bb2c9044c, direct3ddxgi.idxgidevice_createsurface, dxgi/IDXGIDevice::CreateSurface
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
 - IDXGIDevice.CreateSurface
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice::CreateSurface


## -description


Returns a surface. This method is used internally and you should not call it directly in your application.


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb173074(v=VS.85).aspx">DXGI_SURFACE_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/Bb173074(v=VS.85).aspx">DXGI_SURFACE_DESC</a> structure that describes the surface.


### -param NumSurfaces

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of surfaces to create.


### -param Usage

Type: <b><a href="https://msdn.microsoft.com/library/Bb173078(v=VS.85).aspx">DXGI_USAGE</a></b>

A <a href="https://msdn.microsoft.com/library/Bb173078(v=VS.85).aspx">DXGI_USAGE</a> flag that specifies how the surface is expected to be used.


### -param pSharedResource [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb173073(v=VS.85).aspx">DXGI_SHARED_RESOURCE</a>*</b>

An optional pointer to a <a href="https://msdn.microsoft.com/library/Bb173073(v=VS.85).aspx">DXGI_SHARED_RESOURCE</a> structure that contains shared resource information for opening views of such resources.


### -param ppSurface [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>**</b>

The address of an <a href="https://msdn.microsoft.com/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> interface pointer to the first created surface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



The <b>CreateSurface</b> method creates a buffer to exchange data between one or more devices. It is used internally, and you should not directly call it.

The runtime automatically creates an <a href="https://msdn.microsoft.com/library/Bb174565(v=VS.85).aspx">IDXGISurface</a> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface</b> interface when it calls <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> or <a href="https://msdn.microsoft.com/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface</b> interface that represents the 2D texture surface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface</b>. 





## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb173560(v=VS.85).aspx">ID3D10Device::CreateTexture2D</a>



<a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>



<a href="https://msdn.microsoft.com/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>
 

 

