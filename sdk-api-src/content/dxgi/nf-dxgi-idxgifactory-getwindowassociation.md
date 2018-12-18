---
UID: NF:dxgi.IDXGIFactory.GetWindowAssociation
title: IDXGIFactory::GetWindowAssociation
author: windows-sdk-content
description: Get the window through which the user controls the transition to and from full screen.
old-location: direct3ddxgi\idxgifactory_getwindowassociation.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_getwindowassociation.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWindowAssociation, GetWindowAssociation method [DXGI], GetWindowAssociation method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],GetWindowAssociation method, IDXGIFactory.GetWindowAssociation, IDXGIFactory::GetWindowAssociation, b199d248-a0a8-e257-1b89-68baeb809572, direct3ddxgi.idxgifactory_getwindowassociation, dxgi/IDXGIFactory::GetWindowAssociation
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
 - IDXGIFactory.GetWindowAssociation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory::GetWindowAssociation


## -description


Get the window through which the user controls the transition to and from full screen.


## -parameters




### -param pWindowHandle [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>*</b>

A pointer to a window handle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns a code that indicates success or failure. <b>S_OK</b> indicates success, <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a> indicates <i>pWindowHandle</i> was passed in as <b>NULL</b>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>
 

 

