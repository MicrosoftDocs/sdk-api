---
UID: NF:dxgidebug.DXGIGetDebugInterface
title: DXGIGetDebugInterface function (dxgidebug.h)
description: Retrieves a debugging interface.
old-location: direct3ddxgi\dxgigetdebuginterface.htm
tech.root: direct3ddxgi
ms.assetid: 7702B842-6808-4CA9-A5B4-B1A1DC2479A7
ms.date: 12/05/2018
ms.keywords: DXGIGetDebugInterface, DXGIGetDebugInterface function [DXGI], direct3ddxgi.dxgigetdebuginterface, dxgidebug/DXGIGetDebugInterface
f1_keywords:
- dxgidebug/DXGIGetDebugInterface
dev_langs:
- c++
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Dxgidebug.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dxgidebug.dll
api_name:
- DXGIGetDebugInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DXGIGetDebugInterface function


## -description


Retrieves a debugging interface.


## -parameters




### -param riid

The globally unique identifier (GUID) of the requested interface type.


### -param ppDebug

A pointer to a buffer that receives a pointer to the debugging interface.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a> and <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a> are debugging interfaces.

To access <b>DXGIGetDebugInterface</b>, call the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> function to get Dxgidebug.dll and the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to get the address of <b>DXGIGetDebugInterface</b>.<b>Windows 8.1:  </b>Starting in Windows 8.1, Windows Store apps call the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1">DXGIGetDebugInterface1</a> function to get an  <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug1">IDXGIDebug1</a> interface.



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-functions">DXGI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>
 

 

