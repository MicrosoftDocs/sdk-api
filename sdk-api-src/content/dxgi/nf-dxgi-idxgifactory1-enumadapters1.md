---
UID: NF:dxgi.IDXGIFactory1.EnumAdapters1
title: IDXGIFactory1::EnumAdapters1 method
author: windows-driver-content
description: Enumerates both adapters (video cards) with or without outputs.
old-location: direct3ddxgi\idxgifactory1_enumadapters1.htm
old-project: direct3ddxgi
ms.assetid: 351b7b2d-abb7-449e-bee2-eea96fef3b9d
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: 0a909fb2-9d08-a479-d85f-14de8ba21f69, EnumAdapters1 method [DXGI], EnumAdapters1 method [DXGI], IDXGIFactory1 interface, EnumAdapters1,IDXGIFactory1.EnumAdapters1, IDXGIFactory1, IDXGIFactory1 interface [DXGI], EnumAdapters1 method, IDXGIFactory1::EnumAdapters1, direct3ddxgi.idxgifactory1_enumadapters1, dxgi/IDXGIFactory1::EnumAdapters1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIFactory1.EnumAdapters1
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory1::EnumAdapters1 method


## -description


Enumerates both adapters (video cards) with or without outputs.


## -parameters




### -param Adapter

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the adapter to enumerate.


### -param ppAdapter [out]

Type: <b><a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a> interface at the position specified by the <i>Adapter</i> parameter.  
          This parameter must not be <b>NULL</b>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="dxgi_error.htm">DXGI_ERROR_NOT_FOUND</a> if the index is greater than or equal to the number of adapters in the local 
      system, or <a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a> if <i>ppAdapter</i> parameter is <b>NULL</b>.




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

When you create a factory, the factory enumerates the set of adapters that are available in the system. Therefore, if you change the adapters in a system, you must destroy 
      and recreate the <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> object. The number of adapters in a system changes when you add or remove a display card, or dock or undock a laptop. 

When the <b>EnumAdapters1</b> method succeeds and fills the <i>ppAdapter</i> parameter with the address of the pointer to the adapter interface, <b>EnumAdapters1</b> increments the adapter interface's reference count. When you finish using the 
      adapter interface, call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method to decrement the reference count before you destroy the pointer.

<b>EnumAdapters1</b> first returns the adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero. <b>EnumAdapters1</b> next returns other adapters with outputs. <b>EnumAdapters1</b> finally returns adapters without outputs.


#### Examples


          Enumerating Adapters
          

The following code example demonstrates how to enumerate adapters using the <b>EnumAdapters1</b> method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
UINT i = 0; 
IDXGIAdapter1 * pAdapter; 
std::vector &lt;IDXGIAdapter1*&gt; vAdapters; 
while(pFactory-&gt;EnumAdapters1(i, &amp;pAdapter) != DXGI_ERROR_NOT_FOUND) 
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



<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>
 

 

