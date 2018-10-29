---
UID: NF:dxgi.IDXGIFactory.CreateSoftwareAdapter
title: IDXGIFactory::CreateSoftwareAdapter
author: windows-sdk-content
description: Create an adapter interface that represents a software adapter.
old-location: direct3ddxgi\idxgifactory_createsoftwareadapter.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_createsoftwareadapter.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateSoftwareAdapter, CreateSoftwareAdapter method [DXGI], CreateSoftwareAdapter method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],CreateSoftwareAdapter method, IDXGIFactory.CreateSoftwareAdapter, IDXGIFactory::CreateSoftwareAdapter, direct3ddxgi.idxgifactory_createsoftwareadapter, dxgi/IDXGIFactory::CreateSoftwareAdapter, eb1643db-ba87-e9e9-56a9-b7f505fcd700
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
 - IDXGIFactory.CreateSoftwareAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory::CreateSoftwareAdapter


## -description


Create an adapter interface that represents a software adapter.


## -parameters




### -param Module

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

Handle to the software adapter's dll. HMODULE can be obtained with <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> or <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>.


### -param ppAdapter [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>**</b>

Address of a pointer to an adapter (see <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">return code</a> indicating success or failure.




## -remarks



A software adapter is a DLL that implements the entirety of a device driver interface, plus emulation, if necessary, of kernel-mode graphics components for Windows. Details on implementing a software adapter can be found in the Windows Vista Driver Development Kit. This is a very complex development task, and is not recommended for general readers.

Calling this method will increment the module's reference count by one. The reference count can be decremented by calling <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.

The typical calling scenario is to call <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>, pass the handle to <b>CreateSoftwareAdapter</b>, then immediately call <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> on the DLL and forget the DLL's <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a>. Since the software adapter calls <b>FreeLibrary</b> when it is destroyed, the lifetime of the DLL will now be owned by the adapter, and the application is free of any further consideration of its lifetime.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>
 

 

