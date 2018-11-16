---
UID: NF:dxgi1_4.IDXGIFactory4.EnumWarpAdapter
title: IDXGIFactory4::EnumWarpAdapter
author: windows-sdk-content
description: Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
old-location: direct3ddxgi\idxgifactory4_enumwarpadapter.htm
tech.root: direct3ddxgi
ms.assetid: 18991B1A-5FA7-4298-A5FD-C8D7C485E4F7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumWarpAdapter, EnumWarpAdapter method [DXGI], EnumWarpAdapter method [DXGI],IDXGIFactory4 interface, IDXGIFactory4 interface [DXGI],EnumWarpAdapter method, IDXGIFactory4.EnumWarpAdapter, IDXGIFactory4::EnumWarpAdapter, direct3ddxgi.idxgifactory4_enumwarpadapter, dxgi1_4/IDXGIFactory4::EnumWarpAdapter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_4.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory4.EnumWarpAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_4.h
: 
- IDXGIFactory4.EnumWarpAdapter
: 
---

# IDXGIFactory4::EnumWarpAdapter


## -description


Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.
          


### -param ppvAdapter [out]

Type: <b>void**</b>

The address of an <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.
            See also Direct3D 12 Return Codes.
          




## -remarks



For more information, see <a href="https://msdn.microsoft.com/DEA901EA-B0F9-41D9-802C-ED1D6A7888E0">DXGI 1.4 Improvements</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/248CF7CF-BC7D-430F-9EA1-638A42AAC021">IDXGIFactory4</a>
 

 

