---
UID: NF:dxgi1_2.IDXGISwapChain1.GetCoreWindow
title: IDXGISwapChain1::GetCoreWindow
author: windows-sdk-content
description: Retrieves the underlying CoreWindow object for this swap-chain object.
old-location: direct3ddxgi\idxgiswapchain1_getimmersivewindow.htm
old-project: direct3ddxgi
ms.assetid: ABD529CF-41D8-4F21-8F47-D0D053AF2322
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetCoreWindow, GetCoreWindow method [DXGI], GetCoreWindow method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetCoreWindow method, IDXGISwapChain1.GetCoreWindow, IDXGISwapChain1::GetCoreWindow, direct3ddxgi.idxgiswapchain1_getimmersivewindow, dxgi1_2/IDXGISwapChain1::GetCoreWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IDXGISwapChain1.GetCoreWindow
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain1::GetCoreWindow


## -description


Retrieves the underlying <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object for this swap-chain object.


## -parameters




### -param refiid [in]

A pointer to the globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object that is referenced by 
          the <i>ppUnk</i> parameter.


### -param ppUnk [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object.


## -returns



<b>GetCoreWindow</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the underlying <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  if <i>ppUnk</i> is <b>NULL</b>; that is, the swap chain is not associated with a <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object.</li>
<li>Any <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a> that a call to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to query for an <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object might typically return.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic. </li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>GetCoreWindow</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



Applications call the <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a> method to create a swap chain that is associated with an <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

