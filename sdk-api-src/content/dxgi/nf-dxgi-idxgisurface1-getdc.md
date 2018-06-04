---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

