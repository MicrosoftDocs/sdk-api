---
UID: NF:dxgi.IDXGIFactory1.EnumAdapters1
title: IDXGIFactory1::EnumAdapters1 (dxgi.h)
description: Enumerates both adapters (video cards) with or without outputs.
helpviewer_keywords: ["0a909fb2-9d08-a479-d85f-14de8ba21f69","EnumAdapters1","EnumAdapters1 method [DXGI]","EnumAdapters1 method [DXGI]","IDXGIFactory1 interface","IDXGIFactory1 interface [DXGI]","EnumAdapters1 method","IDXGIFactory1.EnumAdapters1","IDXGIFactory1::EnumAdapters1","direct3ddxgi.idxgifactory1_enumadapters1","dxgi/IDXGIFactory1::EnumAdapters1"]
old-location: direct3ddxgi\idxgifactory1_enumadapters1.htm
tech.root: direct3ddxgi
ms.assetid: 351b7b2d-abb7-449e-bee2-eea96fef3b9d
ms.date: 12/05/2018
ms.keywords: 0a909fb2-9d08-a479-d85f-14de8ba21f69, EnumAdapters1, EnumAdapters1 method [DXGI], EnumAdapters1 method [DXGI],IDXGIFactory1 interface, IDXGIFactory1 interface [DXGI],EnumAdapters1 method, IDXGIFactory1.EnumAdapters1, IDXGIFactory1::EnumAdapters1, direct3ddxgi.idxgifactory1_enumadapters1, dxgi/IDXGIFactory1::EnumAdapters1
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIFactory1::EnumAdapters1
 - dxgi/IDXGIFactory1::EnumAdapters1
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
 - IDXGIFactory1.EnumAdapters1
---

# IDXGIFactory1::EnumAdapters1


## -description

Enumerates both adapters (video cards) with or without outputs.

## -parameters

### -param Adapter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the adapter to enumerate.

### -param ppAdapter [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a> interface at the position specified by the <i>Adapter</i> parameter.  
          This parameter must not be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_FOUND</a> if the index is greater than or equal to the number of adapters in the local 
      system, or <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>ppAdapter</i> parameter is <b>NULL</b>.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

When you create a factory, the factory enumerates the set of adapters that are available in the system. Therefore, if you change the adapters in a system, you must destroy 
      and recreate the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a> object. The number of adapters in a system changes when you add or remove a display card, or dock or undock a laptop. 

When the <b>EnumAdapters1</b> method succeeds and fills the <i>ppAdapter</i> parameter with the address of the pointer to the adapter interface, <b>EnumAdapters1</b> increments the adapter interface's reference count. When you finish using the 
      adapter interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to decrement the reference count before you destroy the pointer.

<b>EnumAdapters1</b> first returns the adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero. <b>EnumAdapters1</b> next returns other adapters with outputs. <b>EnumAdapters1</b> finally returns adapters without outputs.


#### Examples

Enumerating Adapters
          

The following code example demonstrates how to enumerate adapters using the <b>EnumAdapters1</b> method.


```

UINT i = 0; 
IDXGIAdapter1 * pAdapter; 
std::vector <IDXGIAdapter1*> vAdapters; 
while(pFactory->EnumAdapters1(i, &pAdapter) != DXGI_ERROR_NOT_FOUND) 
{ 
	vAdapters.push_back(pAdapter); 
	++i; 
} 
          
```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>