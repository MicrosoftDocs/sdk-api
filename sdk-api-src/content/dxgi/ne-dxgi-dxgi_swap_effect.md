---
UID: NE:dxgi.DXGI_SWAP_EFFECT
title: DXGI_SWAP_EFFECT (dxgi.h)
description: Options for handling pixels in a display surface after calling IDXGISwapChain1::Present1.
helpviewer_keywords: ["DXGI_SWAP_EFFECT","DXGI_SWAP_EFFECT enumeration [DXGI]","DXGI_SWAP_EFFECT_DISCARD","DXGI_SWAP_EFFECT_FLIP_DISCARD","DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL","DXGI_SWAP_EFFECT_SEQUENTIAL","c9248b7c-731f-95e1-6c64-22fdef69d697","direct3ddxgi.DXGI_SWAP_EFFECT","dxgi/DXGI_SWAP_EFFECT","dxgi/DXGI_SWAP_EFFECT_DISCARD","dxgi/DXGI_SWAP_EFFECT_FLIP_DISCARD","dxgi/DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL","dxgi/DXGI_SWAP_EFFECT_SEQUENTIAL"]
old-location: direct3ddxgi\DXGI_SWAP_EFFECT.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_swap_effect.htm
ms.date: 12/05/2018
ms.keywords: DXGI_SWAP_EFFECT, DXGI_SWAP_EFFECT enumeration [DXGI], DXGI_SWAP_EFFECT_DISCARD, DXGI_SWAP_EFFECT_FLIP_DISCARD, DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL, DXGI_SWAP_EFFECT_SEQUENTIAL, c9248b7c-731f-95e1-6c64-22fdef69d697, direct3ddxgi.DXGI_SWAP_EFFECT, dxgi/DXGI_SWAP_EFFECT, dxgi/DXGI_SWAP_EFFECT_DISCARD, dxgi/DXGI_SWAP_EFFECT_FLIP_DISCARD, dxgi/DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL, dxgi/DXGI_SWAP_EFFECT_SEQUENTIAL
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_SWAP_EFFECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SWAP_EFFECT
 - dxgi/DXGI_SWAP_EFFECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SWAP_EFFECT
---

## -description

Options for handling pixels in a display surface after calling <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>.

## -enum-fields

### -field DXGI_SWAP_EFFECT_DISCARD:0

Use this flag to specify the bit-block transfer (bitblt) model and to specify that DXGI discard the contents of the back buffer after you call <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>.
            This flag is valid for a swap chain with more than one back buffer, although, applications only have read and write access to buffer 0.
            Use this flag to enable the display driver to select the most efficient presentation technique for the swap chain.
          
<b>Direct3D 12:  </b>This enumeration value is never supported. D3D12 apps must use <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> or <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b>.

<div class="alert"><b>Note</b>  There are differences between full screen exclusive and full screen UWP. If you are porting a Direct3D 11 application to UWP on a Windows PC, be aware that the use of  <b>DXGI_SWAP_EFFECT_DISCARD</b> when creating swap chains does
not behave the same way in UWP as it does in Win32, and its use may be detrimental to GPU performance.

This is because UWP applications are forced into FLIP swap modes (even if other swap modes are set), because this reduces the computation 
time used by the memory copies originally done by the older bitblt model.

The recommended approach is to manually convert DX11 Discard swap chains to use flip models within UWP,  using <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b> instead of <b>DXGI_SWAP_EFFECT_DISCARD</b> where possible.
 Refer to the Example below, and see <a href="/windows/win32/direct3ddxgi/for-best-performance--use-dxgi-flip-model">this article</a> for more information.</div>
<div> </div>

### -field DXGI_SWAP_EFFECT_SEQUENTIAL:1

Use this flag to specify the bitblt model and to specify that DXGI persist the contents of the back buffer after you call <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>.
              Use this option to present the contents of the swap chain in order, from the first buffer (buffer 0) to the last buffer.
              This flag cannot be used with multisampling.
              
<b>Direct3D 12:  </b>This enumeration value is never supported. D3D12 apps must use <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> or <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b>.
            

<div class="alert"><b>Note</b>  For best performance, use <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> instead of <b>DXGI_SWAP_EFFECT_SEQUENTIAL</b>. See <a href="/windows/win32/direct3ddxgi/for-best-performance--use-dxgi-flip-model">this article</a> for more information.</div>
<div> </div>

### -field DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL:3

Use this flag to specify the flip presentation model and to specify that DXGI persist the contents of the back buffer after you call <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>. This flag cannot be used with multisampling.
            

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_SWAP_EFFECT_FLIP_DISCARD:4

Use this flag to specify the flip presentation model and to specify that DXGI discard the contents of the back buffer after you call <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>.
              This flag cannot be used with multisampling and partial presentation.
              See <a href="/windows/win32/direct3ddxgi/dxgi-1-4-improvements">DXGI 1.4 Improvements</a>.
            

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 10. 
This flag is valid for a swap chain with more than one back buffer; although applications have read and write access only to buffer 0.
              

<div class="alert"><b>Note</b>  Windows Store apps must use <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> or <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b>.
            </div>
<div> </div>

## -remarks

This enumeration is used by the <a href="/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a> and <a href="/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structures.
        
In D3D12, only <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> and <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b> are supported, and the bitblt models are not. Because of this, multisampling a back buffer is not supported in D3D12, and you must manually perform multisampling in the app using <b><a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource">ID3D12GraphicsCommandList::ResolveSubresource</a></b> or <b><a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion">ID3D12GraphicsCommandList1::ResolveSubresourceRegion</a></b>.

To use multisampling with <b>DXGI_SWAP_EFFECT_SEQUENTIAL</b> or <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b>, you must perform the multisampling in a separate render target. For example, create a multisampled texture by calling <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> with a filled <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a> structure (<b>BindFlags</b> member set to <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_RENDER_TARGET</a> and <b>SampleDesc</b> member with multisampling parameters). Next call <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">ID3D11Device::CreateRenderTargetView</a> to create a render-target view for the texture, and render your scene into the texture. Finally call <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ID3D11DeviceContext::ResolveSubresource</a> to resolve the multisampled texture into your non-multisampled swap chain.
        

The primary difference between presentation models is how back-buffer contents get to the Desktop Window Manager (DWM) for composition. In the bitblt model, which is used with the <b>DXGI_SWAP_EFFECT_DISCARD</b> and <b>DXGI_SWAP_EFFECT_SEQUENTIAL</b> values, contents of the back buffer get copied into the redirection surface on each call to <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>. In the flip model, which is used with the <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> value, all back buffers are shared with the DWM. Therefore, the DWM can compose straight from those back buffers without any additional copy operations.
          In general, the flip model is the more efficient model. The flip model also provides more features, such as enhanced present statistics.
        
The difference between <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> and <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b> is that <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> forces DXGI to guarantee that the contents of each back buffer is preserved across `IDXGISwapChain::Present` calls, whereas <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b> doesn't provide this guarantee. The compositor, under certain scenarios, can use DirectFlip, where it uses the application's back buffer as the entire display back buffer, which elides the cost of copying the application's back buffer into the final desktop back buffer. With <b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b> and <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b>, this optimization can occur when the application is the only item visible on the screen. However, even when the application is not the only visible item on the screen, if the flip model is <b>DXGI_SWAP_EFFECT_FLIP_DISCARD</b>, the compositor can in some scenarios still perform this optimization, by drawing other content onto the application's back buffer.

When you call <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> on a flip model swap chain (<b>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</b>) with 0 specified in the <i>SyncInterval</i> parameter, <b>IDXGISwapChain1::Present1</b>'s behavior is the same as the behavior of <a href="/windows/win32/direct3darticles/direct3d-9ex-improvements">Direct3D 9Ex</a>'s <a href="/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">IDirect3DDevice9Ex::PresentEx</a> with <a href="/windows/win32/direct3d9/d3dswapeffect">D3DSWAPEFFECT_FLIPEX</a> and <a href="/windows/win32/direct3d9/d3dpresent">D3DPRESENT_FORCEIMMEDIATE</a>. That is, the runtime not only presents the next frame instead of any previously queued frames, it also terminates any remaining time left on the previously queued frames.
        

Regardless of whether the flip model is more efficient, an application still might choose the bitblt model because the bitblt model is the only way to mix GDI and DirectX presentation. In the flip model, the application must create the swap chain with <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE</a>, and then must use <a href="/windows/win32/api/dxgi/nf-dxgi-idxgisurface1-getdc">GetDC</a> on the back buffer explicitly. After the first successful call to <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> on a flip-model swap chain, GDI no longer works with the <a href="/windows/win32/WinProg/windows-data-types">HWND</a> that is associated with that swap chain, even after the destruction of the swap chain. This restriction even extends to methods like <a href="/windows/win32/api/winuser/nf-winuser-scrollwindowex">ScrollWindowEx</a>.
        

To display HDR swapchain buffer formats and color spaces, a flip model is required. Otherwise they get composed (and clipped) in SDR (sRGB with a 0-1 range).
        

For more info about the flip-model swap chain and optimizing presentation, see <a href="/windows/win32/direct3ddxgi/dxgi-1-2-presentation-improvements">Enhancing presentation with the flip model, dirty rectangles, and scrolled areas</a>.
        


#### Examples

To create a swap chain in UWP, you just need to create a new instance of the DX11 template and look at the implementation of <code>DeviceResources::CreateWindowSizeDependentResources</code> in the <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">D3D12 samples</a>.


``` syntax
DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};

       swapChainDesc.Width = lround(m_d3dRenderTargetSize.Width);    // Match the size of the window.
       swapChainDesc.Height = lround(m_d3dRenderTargetSize.Height);
       swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;            // This is the most common swap chain format.
       swapChainDesc.Stereo = false;
       swapChainDesc.SampleDesc.Count = 1;                           // Don't use multi-sampling.
       swapChainDesc.SampleDesc.Quality = 0;
       swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
       swapChainDesc.BufferCount = 2;                                // Use double-buffering to minimize latency.
       swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;     // All Windows Store apps must use a flip effect.
       swapChainDesc.Flags = 2048;
       swapChainDesc.Scaling = scaling;
       swapChainDesc.AlphaMode = DXGI_ALPHA_MODE_IGNORE;

       // This sequence obtains the DXGI factory that was used to create the Direct3D device above.
       ComPtr<IDXGIDevice3> dxgiDevice;
       DX::ThrowIfFailed(m_d3dDevice.As(&dxgiDevice));

       ComPtr<IDXGIAdapter> dxgiAdapter;
       DX::ThrowIfFailed(dxgiDevice->GetAdapter(&dxgiAdapter));

       ComPtr<IDXGIFactory4> dxgiFactory;
       DX::ThrowIfFailed(dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory)));

       ComPtr<IDXGISwapChain1> swapChain;
       DX::ThrowIfFailed(
              dxgiFactory->CreateSwapChainForCoreWindow(
                     m_d3dDevice.Get(),
                     reinterpret_cast<IUnknown*>(m_window.Get()),
                     &swapChainDesc,
                     nullptr,
                     &swapChain
                     )
              );

```


## -see-also

<a href="/windows/win32/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="https://devblogs.microsoft.com/directx/dxgi-flip-model/">For best performance, use DXGI flip model</a>

