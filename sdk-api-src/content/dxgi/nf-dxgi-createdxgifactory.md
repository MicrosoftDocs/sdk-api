---
UID: NF:dxgi.CreateDXGIFactory
title: CreateDXGIFactory function
author: windows-sdk-content
description: Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.
old-location: direct3ddxgi\createdxgifactory.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\createdxgifactory.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateDXGIFactory, CreateDXGIFactory function [DXGI], direct3ddxgi.createdxgifactory, dxgi/CreateDXGIFactory, f8906daa-c399-a76f-d487-e1f2ee03b8a8
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - DllExport
api_location:
 - DXGI.dll
api_name:
 - CreateDXGIFactory
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: DXGI.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# CreateDXGIFactory function


## -description


Creates a DXGI 1.0 factory that you can use to generate other  DXGI objects.


## -parameters




### -param riid

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a> object referenced by the <i>ppFactory</i> parameter.


### -param ppFactory [out]

Type: <b>void**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a> object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



Use a DXGI factory to generate objects that <a href="https://msdn.microsoft.com/library/Bb174538(v=VS.85).aspx">enumerate adapters</a>, <a href="https://msdn.microsoft.com/library/Bb174537(v=VS.85).aspx">create swap chains</a>, and <a href="https://msdn.microsoft.com/library/Bb174540(v=VS.85).aspx">associate a window</a> with the alt+enter key sequence for toggling to and from the fullscreen display mode.

If the <b>CreateDXGIFactory</b> function succeeds, the reference count on the <a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a> interface is incremented. To avoid a memory leak, when you finish using the interface, call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IDXGIFactory::Release</a> method to release the interface.

<div class="alert"><b>Note</b>  Do not mix the use of DXGI 1.0 (<a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>) and DXGI 1.1 (<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>CreateDXGIFactory</b> fails if your app's <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function calls it. For more info about how DXGI responds from <b>DllMain</b>, see <a href="https://msdn.microsoft.com/library/Bb205075(v=VS.85).aspx">DXGI Responses from DLLMain</a>.</div>
<div> </div>
<div class="alert"><b>Note</b>  Starting with Windows 8, all DXGI factories (regardless if they were created with <b>CreateDXGIFactory</b> or <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a>) enumerate adapters identically. The enumeration order of adapters, which you retrieve with <a href="https://msdn.microsoft.com/library/Bb174538(v=VS.85).aspx">IDXGIFactory::EnumAdapters</a> or <a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">IDXGIFactory1::EnumAdapters1</a>, is as follows: <ul>
<li>Adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero.</li>
<li>Adapters with outputs.</li>
<li>Adapters without outputs.</li>
</ul>
</div>
<div> </div>
The <b>CreateDXGIFactory</b> function does not exist for Windows Store apps. Instead, Windows Store apps use the  <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a> function.


#### Examples


          Creating a DXGI 1.0 Factory
          

The following code example demonstrates how to create a DXGI 1.0 factory.  This example uses the __uuidof() intrinsic to obtain the REFIID, or GUID, of the <a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a> interface.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDXGIFactory * pFactory;
HRESULT hr = CreateDXGIFactory(__uuidof(IDXGIFactory), (void**)(&amp;pFactory) );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>
 

 

