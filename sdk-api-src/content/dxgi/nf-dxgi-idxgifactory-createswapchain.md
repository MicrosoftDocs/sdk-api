---
UID: NF:dxgi.IDXGIFactory.CreateSwapChain
title: IDXGIFactory::CreateSwapChain
author: windows-sdk-content
description: Creates a swap chain.
old-location: direct3ddxgi\idxgifactory_createswapchain.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_createswapchain.htm
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CreateSwapChain, CreateSwapChain method [DXGI], CreateSwapChain method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],CreateSwapChain method, IDXGIFactory.CreateSwapChain, IDXGIFactory::CreateSwapChain, adabc9a1-e4c0-9260-1e58-bd7acac73fd8, direct3ddxgi.idxgifactory_createswapchain, dxgi/IDXGIFactory::CreateSwapChain
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDXGIFactory.CreateSwapChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory::CreateSwapChain


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>CreateSwapChain</b> anymore to create a swap chain. Instead, use <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a> depending on how you want to create the swap chain.]

Creates a swap chain.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>) . This parameter cannot be <b>NULL</b>.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a>*</b>

A pointer to a  <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.


### -param ppSwapChain [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>**</b>

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a> interface for the swap chain that <b>CreateSwapChain</b> creates.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a>  if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>, DXGI_STATUS_OCCLUDED if you request full-screen mode and it is unavailable, or E_OUTOFMEMORY. Other error codes defined by the type of device passed in may also be returned.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
If you attempt to create a swap chain in full-screen mode, and full-screen mode is unavailable, the swap chain will be created in windowed mode and DXGI_STATUS_OCCLUDED will be returned.

If the buffer width or the buffer height is zero, the sizes will be inferred from the output window size in the swap-chain description.

Because the target output can't be chosen explicitly when the swap chain is created, we recommend not to create a full-screen swap chain. This can reduce presentation performance if the swap chain size and the output window size do not match. Here are two ways to ensure that the sizes match:

<ul>
<li>Create a windowed swap chain and then set it full-screen using <a href="https://msdn.microsoft.com/en-us/library/Bb174579(v=VS.85).aspx">IDXGISwapChain::SetFullscreenState</a>.</li>
<li>Save a pointer to the swap chain immediately after creation, and use it to get the output window size during a WM_SIZE event. Then resize the swap chain buffers (with <a href="https://msdn.microsoft.com/en-us/library/Bb174577(v=VS.85).aspx">IDXGISwapChain::ResizeBuffers</a>) during the transition from windowed to full-screen.</li>
</ul>
If the swap chain is in full-screen mode, before you release it you must use <a href="https://msdn.microsoft.com/en-us/library/Bb174579(v=VS.85).aspx">SetFullscreenState</a> to switch it to windowed mode. For more information about releasing a swap chain, see the "Destroying a Swap Chain" section of <a href="https://msdn.microsoft.com/en-us/library/Bb205075(v=VS.85).aspx">DXGI Overview</a>.

After the runtime renders the initial frame in full screen, the runtime might unexpectedly exit full screen during a call to <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>. To work around this issue, we recommend that you execute the following code right after you call <b>CreateSwapChain</b> to create a full-screen swap chain (<b>Windowed</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a> set to <b>FALSE</b>).



```

// Detect if newly created full-screen swap chain isn't actually full screen.
IDXGIOutput* pTarget; BOOL bFullscreen;
if (SUCCEEDED(pSwapChain->GetFullscreenState(&bFullscreen, &pTarget)))
{
   pTarget->Release();
}
else
   bFullscreen = FALSE;
// If not full screen, enable full screen again.
if (!bFullscreen)
{
   ShowWindow(hWnd, SW_MINIMIZE);
   ShowWindow(hWnd, SW_RESTORE);
   pSwapChain->SetFullscreenState(TRUE, NULL);
}

```


You can specify <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG</a> values in the swap-chain description that <i>pDesc</i> points to. These values allow you to use features like flip-model presentation and content protection by using pre-Windows 8 APIs.

However, to use stereo presentation and to change resize behavior for the flip model, applications must use the <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a> method. Otherwise, the back-buffer contents implicitly scale to fit the presentation target size; that is, you can't turn off scaling.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app calls <b>CreateSwapChain</b> with full screen specified, <b>CreateSwapChain</b> fails.

Windows Store apps call the  <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a> method to create a swap chain.

For info about how to choose a format for the swap chain's back buffer, see <a href="https://msdn.microsoft.com/1DD8E2D3-430F-4EE4-9C41-78736C904920">Converting data for the color space</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1">For best performance, use DXGI flip model</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>
 

 

