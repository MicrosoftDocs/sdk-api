---
UID: NN:dxgi.IDXGIFactory1
title: IDXGIFactory1
author: windows-driver-content
description: The IDXGIFactory1 interface implements methods for generating DXGI objects.
old-location: direct3ddxgi\idxgifactory1.htm
old-project: direct3ddxgi
ms.assetid: 271f1877-25a7-4d32-9ffa-cb174b366b74
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: 57d28dd0-2a8f-0523-2200-4d14c74f01d6, IDXGIFactory1, IDXGIFactory1 interface [DXGI], IDXGIFactory1 interface [DXGI],described, direct3ddxgi.idxgifactory1, dxgi/IDXGIFactory1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IDXGIFactory1
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory1 interface


## -description


The <b>IDXGIFactory1</b> interface implements methods for generating DXGI objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory1</b> interface inherits from <a href="https://msdn.microsoft.com/642aac36-ca5a-4c62-b5cb-f9d35965ca2f">IDXGIFactory</a>. <b>IDXGIFactory1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIFactory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/351b7b2d-abb7-449e-bee2-eea96fef3b9d">EnumAdapters1</a>
</td>
<td align="left" width="63%">
Enumerates both adapters (video cards) with or without outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1337b20-85c2-48e1-9205-aa729c0d0edc">IsCurrent</a>
</td>
<td align="left" width="63%">
Informs an application of the possible need to re-enumerate adapters.

</td>
</tr>
</table> 


## -remarks



This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

To create a factory, call the <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a> function.

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
You can request the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> or <a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a> interface from the Direct3D device and then use the <a href="https://msdn.microsoft.com/7e7f7494-445e-4bf1-8b94-fc40b7d9b887">IDXGIObject::GetParent</a> method to locate 
the factory.  The following code shows how.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIDevice1 * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice1), (void **)&amp;pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice-&gt;GetParent(__uuidof(IDXGIAdapter), (void **)&amp;pDXGIAdapter);

IDXGIFactory1 * pIDXGIFactory;
pDXGIAdapter-&gt;GetParent(__uuidof(IDXGIFactory1), (void **)&amp;pIDXGIFactory);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/642aac36-ca5a-4c62-b5cb-f9d35965ca2f">IDXGIFactory</a>
 

 

