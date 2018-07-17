---
UID: NF:dxgi1_2.IDXGIFactory2.CreateSwapChainForComposition
title: IDXGIFactory2::CreateSwapChainForComposition
author: windows-sdk-content
description: Creates a swap chain that you can use to send Direct3D content into the DirectComposition API or the Windows.UI.Xaml framework to compose in a window.
old-location: direct3ddxgi\idxgifactory2_createswapchainforcompositionsurface.htm
old-project: direct3ddxgi
ms.assetid: 8AE13082-F8C3-422A-A111-4E91488BD1AF
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CreateSwapChainForComposition, CreateSwapChainForComposition method [DXGI], CreateSwapChainForComposition method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],CreateSwapChainForComposition method, IDXGIFactory2.CreateSwapChainForComposition, IDXGIFactory2::CreateSwapChainForComposition, direct3ddxgi.idxgifactory2_createswapchainforcompositionsurface, dxgi1_2/IDXGIFactory2::CreateSwapChainForComposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.CreateSwapChainForComposition
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory2::CreateSwapChainForComposition


## -description


Creates a swap chain that you can use to send Direct3D content into the <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> API or the <a href="https://msdn.microsoft.com/e41c3007-8e8d-4c37-b098-dc5bcca39302">Windows.UI.Xaml</a> framework to compose in a window.


## -parameters




### -param pDevice [in]

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>). This parameter cannot be <b>NULL</b>. Software drivers, like <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE_REFERENCE</a>, are not supported for composition swap chains.


### -param pDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.

You must specify the <a href="https://msdn.microsoft.com/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> because <b>CreateSwapChainForComposition</b> supports only <a href="https://msdn.microsoft.com/E132DAF5-80B7-4C52-A760-3779CC140CE7">flip presentation model</a>.

You must also specify the <a href="https://msdn.microsoft.com/library/Hh404526(v=VS.85).aspx">DXGI_SCALING_STRETCH</a> value in the <b>Scaling</b> member of <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a>.


### -param pRestrictToOutput [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a> interface for the output to restrict content to. You must also pass the <a href="https://msdn.microsoft.com/library/Bb509554(v=VS.85).aspx">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.


Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.


### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a> interface for the swap chain that <b>CreateSwapChainForComposition</b> creates.


## -returns



<b>CreateSwapChainForComposition</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>CreateSwapChainForComposition</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



You can use composition swap chains with either <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a>’s <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a> interface or XAML’s <a href="https://msdn.microsoft.com/77F5EB53-0DF9-4BA7-810C-9B7B073E76A7">SwapChainBackgroundPanel</a> class. For DirectComposition, you can call the <a href="https://msdn.microsoft.com/894E6E30-6C28-476D-9AE5-D0664A69E03C">IDCompositionVisual::SetContent</a> method to set the swap chain as the content of a <a href="https://msdn.microsoft.com/F442BDCA-C913-4438-BFFA-D3F28B68EE85">visual object</a>, which then allows you to bind the swap chain to the visual tree. For XAML, the <b>SwapChainBackgroundPanel</b> class exposes a classic COM interface <b>ISwapChainBackgroundPanelNative</b>. You can use the <a href="https://msdn.microsoft.com/EDAEA67F-78CD-49F8-84FC-A7037629239A">ISwapChainBackgroundPanelNative::SetSwapChain</a> method to bind to the XAML UI graph. For info about how to use composition swap chains with XAML’s <b>SwapChainBackgroundPanel</b> class, see <a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>.

The <a href="https://msdn.microsoft.com/library/Bb174579(v=VS.85).aspx">IDXGISwapChain::SetFullscreenState</a>, <a href="https://msdn.microsoft.com/library/Bb174578(v=VS.85).aspx">IDXGISwapChain::ResizeTarget</a>, <a href="https://msdn.microsoft.com/library/Bb174571(v=VS.85).aspx">IDXGISwapChain::GetContainingOutput</a>, <a href="https://msdn.microsoft.com/C1690710-FA63-4841-B3E2-68200E0B7B23">IDXGISwapChain1::GetHwnd</a>, and <a href="https://msdn.microsoft.com/ABD529CF-41D8-4F21-8F47-D0D053AF2322">IDXGISwapChain::GetCoreWindow</a> methods aren't valid on this type of swap chain. If you call any of these methods on this type of swap chain, they fail.

For info about how to choose a format for the swap chain's back buffer, see <a href="https://msdn.microsoft.com/1DD8E2D3-430F-4EE4-9C41-78736C904920">Converting data for the color space</a>.


#### Examples

The following code example shows how to use <b>CreateSwapChainForComposition</b> in the <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> API or the <a href="https://msdn.microsoft.com/e41c3007-8e8d-4c37-b098-dc5bcca39302">Windows.UI.Xaml</a> framework:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGISwapChain1 *pSwapChain = NULL;
pDXGIFactory-&gt;CreateSwapChainForComposition( pD3DDevice, 
    SwapChainDescription, NULL, &amp;pSwapChain);

// DComp
IDCompositionVisual *pDCompVisual = NULL;
pDCompDevice-&gt;CreateVisual( &amp;pDCompVisual );
pDCompVisual-&gt;SetContent( pSwapChain );

// XAML
virtual HRESULT STDMETHODCALLTYPE OnLaunched( __RPC__in_opt ILaunchActivatedEventArgs *args)
{
    const wchar_t *pXaml =
    L"&lt;SwapChainBackgroundPanel xmlns='http://schemas.microsoft.com/winfx/2006/xaml/presentation' x:Name='root' "
    L" xmlns:x='http://schemas.microsoft.com/winfx/2006/xaml'&gt; "
    L"&lt;/SwapChainBackgroundPanel&gt;";
    LoadXaml( pXaml );

    ComPtr&lt;ISwapChainBackgroundPanel&gt; spSwapChainBackgroundPanel;
    FindName&lt;Windows::UI::Xaml::Controls::ISwapChainBackgroundPanel&gt;(
            L"root",
            &amp;spSwapChainBackgroundPanel
            );

    ComPtr&lt;ISwapChainBackgroundPanelNative&gt; spSwapChainBackgroundPanelNative;
    spSwapChainBackgroundPanel.As&lt;ISwapChainBackgroundPanelNative&gt;(&amp;spSwapChainBackgroundPanelNative);
    spSwapChainBackgroundPanelNative-&gt;SetSwapChain( pSwapChain );
}
</pre>
</td>
</tr>
</table></span></div>
The <a href="https://msdn.microsoft.com/77F5EB53-0DF9-4BA7-810C-9B7B073E76A7">ISwapChainBackgroundPanelNative</a> interface is declared in the windows.ui.xaml.media.dxinterop.h header.




## -see-also




<a href="https://msdn.microsoft.com/library/Mt846759(v=VS.85).aspx">For best performance, use DXGI flip model</a>



<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

