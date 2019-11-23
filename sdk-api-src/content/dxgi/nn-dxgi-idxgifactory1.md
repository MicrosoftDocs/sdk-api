---
UID: NN:dxgi.IDXGIFactory1
title: IDXGIFactory1 (dxgi.h)

description: The IDXGIFactory1 interface implements methods for generating DXGI objects.
old-location: direct3ddxgi\idxgifactory1.htm
tech.root: direct3ddxgi
ms.assetid: 271f1877-25a7-4d32-9ffa-cb174b366b74

ms.date: 12/05/2018
ms.keywords: 57d28dd0-2a8f-0523-2200-4d14c74f01d6, IDXGIFactory1, IDXGIFactory1 interface [DXGI], IDXGIFactory1 interface [DXGI],described, direct3ddxgi.idxgifactory1, dxgi/IDXGIFactory1
ms.topic: interface
f1_keywords: 
 - "dxgi/IDXGIFactory1"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIFactory1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory1 interface


## -description


The <b>IDXGIFactory1</b> interface implements methods for generating DXGI objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>. <b>IDXGIFactory1</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">EnumAdapters1</a>
</td>
<td align="left" width="63%">
Enumerates both adapters (video cards) with or without outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-iscurrent">IsCurrent</a>
</td>
<td align="left" width="63%">
Informs an application of the possible need to re-enumerate adapters.

</td>
</tr>
</table> 


## -remarks



This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

To create a factory, call the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> function.

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
You can request the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a> interface from the Direct3D device and then use the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate 
the factory.  The following code shows how.


```
IDXGIDevice1 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice1), (void **)&pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice->GetParent(__uuidof(IDXGIAdapter), (void **)&pDXGIAdapter);

IDXGIFactory1 * pIDXGIFactory;
pDXGIAdapter->GetParent(__uuidof(IDXGIFactory1), (void **)&pIDXGIFactory);

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>
 

 

