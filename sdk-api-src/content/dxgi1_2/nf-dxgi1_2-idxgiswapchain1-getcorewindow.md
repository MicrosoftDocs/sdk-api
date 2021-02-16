---
UID: NF:dxgi1_2.IDXGISwapChain1.GetCoreWindow
title: IDXGISwapChain1::GetCoreWindow (dxgi1_2.h)
description: Retrieves the underlying CoreWindow object for this swap-chain object.
helpviewer_keywords: ["GetCoreWindow","GetCoreWindow method [DXGI]","GetCoreWindow method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetCoreWindow method","IDXGISwapChain1.GetCoreWindow","IDXGISwapChain1::GetCoreWindow","direct3ddxgi.idxgiswapchain1_getimmersivewindow","dxgi1_2/IDXGISwapChain1::GetCoreWindow"]
old-location: direct3ddxgi\idxgiswapchain1_getimmersivewindow.htm
tech.root: direct3ddxgi
ms.assetid: ABD529CF-41D8-4F21-8F47-D0D053AF2322
ms.date: 12/05/2018
ms.keywords: GetCoreWindow, GetCoreWindow method [DXGI], GetCoreWindow method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetCoreWindow method, IDXGISwapChain1.GetCoreWindow, IDXGISwapChain1::GetCoreWindow, direct3ddxgi.idxgiswapchain1_getimmersivewindow, dxgi1_2/IDXGISwapChain1::GetCoreWindow
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain1::GetCoreWindow
 - dxgi1_2/IDXGISwapChain1::GetCoreWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.GetCoreWindow
---

# IDXGISwapChain1::GetCoreWindow


## -description

Retrieves the underlying <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object for this swap-chain object.

## -parameters

### -param refiid [in]

A pointer to the globally unique identifier (GUID) of the <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object that is referenced by 
          the <i>ppUnk</i> parameter.

### -param ppUnk [out]

A pointer to a variable that receives a pointer to the <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object.

## -returns

<b>GetCoreWindow</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the underlying <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if <i>ppUnk</i> is <b>NULL</b>; that is, the swap chain is not associated with a <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object.</li>
<li>Any <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> that a call to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to query for an <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object might typically return.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic. </li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>GetCoreWindow</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

Applications call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a> method to create a swap chain that is associated with an <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> object.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>