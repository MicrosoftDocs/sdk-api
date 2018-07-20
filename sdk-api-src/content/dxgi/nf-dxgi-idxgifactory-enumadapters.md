---
UID: NF:dxgi.IDXGIFactory.EnumAdapters
title: IDXGIFactory::EnumAdapters
author: windows-sdk-content
description: Enumerates the adapters (video cards).
old-location: direct3ddxgi\idxgifactory_enumadapters.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_enumadapters.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 457b8c88-be8c-c241-7864-e16ac2622ee0, EnumAdapters, EnumAdapters method [DXGI], EnumAdapters method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],EnumAdapters method, IDXGIFactory.EnumAdapters, IDXGIFactory::EnumAdapters, direct3ddxgi.idxgifactory_enumadapters, dxgi/IDXGIFactory::EnumAdapters
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
 - IDXGIFactory.EnumAdapters
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory::EnumAdapters


## -description


Enumerates the adapters (video cards).


## -parameters




### -param Adapter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the adapter to enumerate.


### -param ppAdapter [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> interface at the position specified by the <i>Adapter</i> parameter.  This parameter must not be <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_FOUND</a> if the index is greater than or equal to the number of adapters in the local system, or <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a> if <i>ppAdapter</i> parameter is <b>NULL</b>.




## -remarks



When you create a factory, the factory enumerates the set of adapters that are available in the system. Therefore, if you change the adapters in a system, you must destroy 
      and recreate the <a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a> object. The number of adapters in a system changes when you add or remove a display card, or dock or undock a laptop. 

When the <b>EnumAdapters</b> method succeeds and fills the <i>ppAdapter</i> parameter with the address of the pointer to the adapter interface, <b>EnumAdapters</b> increments the adapter interface's reference count. When you finish using the 
      adapter interface, call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to decrement the reference count before you destroy the pointer.

<b>EnumAdapters</b> first returns the adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero. <b>EnumAdapters</b> next returns other adapters with outputs. <b>EnumAdapters</b> finally returns adapters without outputs.




#### Examples

Enumerating Adapters
          

The following code example demonstrates how to enumerate adapters using the <b>EnumAdapters</b> method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UINT i = 0; 
IDXGIAdapter * pAdapter; 
std::vector &lt;IDXGIAdapter*&gt; vAdapters; 
while(pFactory-&gt;EnumAdapters(i, &amp;pAdapter) != DXGI_ERROR_NOT_FOUND) 
{ 
	vAdapters.push_back(pAdapter); 
	++i; 
} 
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>
 

 

