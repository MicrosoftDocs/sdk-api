---
UID: NF:dxgi.IDXGISurface1.GetDC
title: IDXGISurface1::GetDC
author: windows-sdk-content
description: Returns a device context (DC) that allows you to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface using Windows Graphics Device Interface (GDI).
old-location: direct3ddxgi\idxgisurface1_getdc.htm
tech.root: direct3ddxgi
ms.assetid: b148d2b4-36a2-46b9-8a98-9f3c478549a4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDC, GetDC method [DXGI], GetDC method [DXGI],IDXGISurface1 interface, IDXGISurface1 interface [DXGI],GetDC method, IDXGISurface1.GetDC, IDXGISurface1::GetDC, aa5d4cb4-dcad-b7fd-560c-12cc222965a0, direct3ddxgi.idxgisurface1_getdc, dxgi/IDXGISurface1::GetDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDXGISurface1.GetDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISurface1::GetDC


## -description


Returns a device context (DC) that allows you to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface using Windows Graphics Device Interface (GDI).


## -parameters




### -param Discard

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that specifies whether to preserve Direct3D contents in the GDI DC. <b>TRUE</b> directs the runtime not to preserve Direct3D contents in the GDI DC; that is, the runtime discards the Direct3D contents. <b>FALSE</b> guarantees that Direct3D contents are available in the GDI DC.


### -param phdc [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a> handle that represents the current device context for GDI rendering.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, an error code.




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

After you use the <b>GetDC</b> method to retrieve a DC, you can render to the DXGI surface by using GDI.  
      The <b>GetDC</b> method readies the surface for GDI rendering and allows inter-operation between DXGI and GDI technologies.  

Keep the following in mind when using this method:

<ul>
<li>You must create the surface by using the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_GDI_COMPATIBLE</a> flag for a surface or by using the <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE</a> flag for swap chains, 
        otherwise this method fails.</li>
<li>You must release the device and call the <a href="https://msdn.microsoft.com/2c3a0cf3-c970-4908-a960-ba261756bd5f">IDXGISurface1::ReleaseDC</a> method before you issue any new Direct3D commands.</li>
<li>This method fails if an outstanding DC has already been created by this method.</li>
<li>The format for the surface or swap chain must be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</a> or <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM</a>.</li>
<li>On <b>GetDC</b>, the render target in the output merger of the Direct3D pipeline is unbound from the surface.  
        You must call the <a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">ID3D11DeviceContext::OMSetRenderTargets</a> method on the device prior to Direct3D rendering after GDI rendering.</li>
<li>Prior to resizing buffers you must release all outstanding DCs.</li>
</ul>
You can also call <b>GetDC</b> on the back buffer at index 0 of a swap chain by obtaining an <a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a>  from the swap chain.  
      The following code illustrates the process.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDXGISwapChain* g_pSwapChain = NULL;
IDXGISurface1* g_pSurface1 = NULL;
...
//Setup the device and and swapchain
g_pSwapChain-&gt;GetBuffer(0, __uuidof(IDXGISurface1), (void**) &amp;g_pSurface1);
g_pSurface1-&gt;GetDC( FALSE, &amp;g_hDC );
...      
//Draw on the DC using GDI
...
//When finish drawing release the DC
g_pSurface1-&gt;ReleaseDC( NULL );
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a>
 

 

