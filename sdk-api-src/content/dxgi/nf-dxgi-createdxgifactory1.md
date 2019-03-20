---
UID: NF:dxgi.CreateDXGIFactory1
title: CreateDXGIFactory1 function (dxgi.h)
author: windows-sdk-content
description: Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.
old-location: direct3ddxgi\createdxgifactory1.htm
tech.root: direct3ddxgi
ms.assetid: 6fb9d7a3-0b59-4b7a-8871-b99d59811d46
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDXGIFactory1, CreateDXGIFactory1 function [DXGI], cbbcd6f0-23c8-ef1c-0d0c-2b56092eb8b1, direct3ddxgi.createdxgifactory1, dxgi/CreateDXGIFactory1
ms.topic: function
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
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxgi.dll
api_name:
 - CreateDXGIFactory1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDXGIFactory1 function


## -description


Creates a DXGI 1.1 factory that you can use to generate other  DXGI objects.


## -parameters




### -param riid

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> object referenced by 
          the <i>ppFactory</i> parameter.


### -param ppFactory [out]

Type: <b>void**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



Use a DXGI 1.1 factory to generate objects that <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">enumerate adapters</a>, 
      <a href="https://msdn.microsoft.com/en-us/library/Bb174537(v=VS.85).aspx">create swap chains</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb174540(v=VS.85).aspx">associate a window</a> with 
      the alt+enter key sequence for toggling to and from the full-screen display mode.  

If the <b>CreateDXGIFactory1</b> function succeeds, the reference count on the <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> interface is incremented. To avoid a memory leak, when you finish using the interface, call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IDXGIFactory1::Release</a> method to release the interface.

This entry point is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

<div class="alert"><b>Note</b>  Do not mix the use of DXGI 1.0 (<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>) and DXGI 1.1 (<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>CreateDXGIFactory1</b> fails if your app's <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function calls it. For more info about how DXGI responds from <b>DllMain</b>, see <a href="https://msdn.microsoft.com/en-us/library/Bb205075(v=VS.85).aspx">DXGI Responses from DLLMain</a>.</div>
<div> </div>
<div class="alert"><b>Note</b>  Starting with Windows 8, all DXGI factories (regardless if they were created with <a href="https://msdn.microsoft.com/en-us/library/Bb204862(v=VS.85).aspx">CreateDXGIFactory</a> or <b>CreateDXGIFactory1</b>) enumerate adapters identically. The enumeration order of adapters, which you retrieve with <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">IDXGIFactory::EnumAdapters</a> or <a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">IDXGIFactory1::EnumAdapters1</a>, is as follows: <ul>
<li>Adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero.</li>
<li>Adapters with outputs.</li>
<li>Adapters without outputs.</li>
</ul>
</div>
<div> </div>

#### Examples

Creating a DXGI 1.1 Factory
          

The following code example demonstrates how to create a DXGI 1.1 factory.  This example uses the __uuidof() intrinsic to 
          obtain the REFIID, or GUID, of the <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> interface.


```

IDXGIFactory1 * pFactory;
HRESULT hr = CreateDXGIFactory1(__uuidof(IDXGIFactory1), (void**)(&pFactory) );
          
```


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>
 

 

