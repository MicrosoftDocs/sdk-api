---
UID: NF:dxgi.IDXGIFactory.CreateSoftwareAdapter
title: IDXGIFactory::CreateSoftwareAdapter (dxgi.h)
description: Create an adapter interface that represents a software adapter.
helpviewer_keywords: ["CreateSoftwareAdapter","CreateSoftwareAdapter method [DXGI]","CreateSoftwareAdapter method [DXGI]","IDXGIFactory interface","IDXGIFactory interface [DXGI]","CreateSoftwareAdapter method","IDXGIFactory.CreateSoftwareAdapter","IDXGIFactory::CreateSoftwareAdapter","direct3ddxgi.idxgifactory_createsoftwareadapter","dxgi/IDXGIFactory::CreateSoftwareAdapter","eb1643db-ba87-e9e9-56a9-b7f505fcd700"]
old-location: direct3ddxgi\idxgifactory_createsoftwareadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_createsoftwareadapter.htm
ms.date: 12/05/2018
ms.keywords: CreateSoftwareAdapter, CreateSoftwareAdapter method [DXGI], CreateSoftwareAdapter method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],CreateSoftwareAdapter method, IDXGIFactory.CreateSoftwareAdapter, IDXGIFactory::CreateSoftwareAdapter, direct3ddxgi.idxgifactory_createsoftwareadapter, dxgi/IDXGIFactory::CreateSoftwareAdapter, eb1643db-ba87-e9e9-56a9-b7f505fcd700
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory::CreateSoftwareAdapter
 - dxgi/IDXGIFactory::CreateSoftwareAdapter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIFactory.CreateSoftwareAdapter
---

# IDXGIFactory::CreateSoftwareAdapter


## -description

Create an adapter interface that represents a software adapter.

## -parameters

### -param Module

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

Handle to the software adapter's dll. HMODULE can be obtained with <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>.

### -param ppAdapter [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>**</b>

Address of a pointer to an adapter (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

A <a href="/windows/desktop/direct3ddxgi/dxgi-error">return code</a> indicating success or failure.

## -remarks

A software adapter is a DLL that implements the entirety of a device driver interface, plus emulation, if necessary, of kernel-mode graphics components for Windows. Details on implementing a software adapter can be found in the Windows Vista Driver Development Kit. This is a very complex development task, and is not recommended for general readers.

Calling this method will increment the module's reference count by one. The reference count can be decremented by calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>.

The typical calling scenario is to call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>, pass the handle to <b>CreateSoftwareAdapter</b>, then immediately call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> on the DLL and forget the DLL's <a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a>. Since the software adapter calls <b>FreeLibrary</b> when it is destroyed, the lifetime of the DLL will now be owned by the adapter, and the application is free of any further consideration of its lifetime.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>