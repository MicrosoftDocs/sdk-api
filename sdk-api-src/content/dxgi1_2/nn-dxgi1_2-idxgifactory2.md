---
UID: NN:dxgi1_2.IDXGIFactory2
title: IDXGIFactory2
author: windows-sdk-content
description: The IDXGIFactory2 interface includes methods to create a newer version swap chain with more features than IDXGISwapChain and to monitor stereoscopic 3D capabilities.
old-location: direct3ddxgi\idxgifactory2.htm
old-project: direct3ddxgi
ms.assetid: D4F210E1-E184-410A-947A-22ED47B3E9F3
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIFactory2, IDXGIFactory2 interface [DXGI], IDXGIFactory2 interface [DXGI],described, direct3ddxgi.idxgifactory2, dxgi1_2/IDXGIFactory2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dxgi.lib
-	Dxgi.dll
api_name:
-	IDXGIFactory2
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory2 interface


## -description



        The <b>IDXGIFactory2</b> interface includes methods to create a newer version swap chain with more features than <a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a> and to monitor stereoscopic 3D capabilities.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory2</b> interface inherits from <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>. <b>IDXGIFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a>
</td>
<td align="left" width="63%">
Creates a swap chain that you can use to send Direct3D content into the <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> API or the <a href="https://msdn.microsoft.com/e41c3007-8e8d-4c37-b098-dc5bcca39302">Windows.UI.Xaml</a> framework to compose in a window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a>
</td>
<td align="left" width="63%">
Creates a swap chain that is associated with the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object for the output window for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">CreateSwapChainForHwnd</a>
</td>
<td align="left" width="63%">
Creates a swap chain that is associated with an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> handle to the output window for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/278F1C2B-6DE7-4D4A-8C6E-10B1004B8EFC">GetSharedResourceAdapterLuid</a>
</td>
<td align="left" width="63%">
Identifies the adapter on which a shared resource object was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81DA1DD6-7D36-4848-ADCB-1F7B765B0A62">IsWindowedStereoEnabled</a>
</td>
<td align="left" width="63%">
Determines whether to use stereo mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DCB6309-C1FF-403F-94E1-ABA769D18170">RegisterOcclusionStatusEvent</a>
</td>
<td align="left" width="63%">
Registers to receive notification of  changes in occlusion status by using event signaling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E8E3C2A-F973-4DC3-A226-DB3FF32F9CC4">RegisterOcclusionStatusWindow</a>
</td>
<td align="left" width="63%">
Registers an application window to receive notification messages of changes of occlusion status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/912FC8B0-8B66-4203-BF27-8D7186F7CAC0">RegisterStereoStatusEvent</a>
</td>
<td align="left" width="63%">
Registers to receive notification of changes in stereo status by using event signaling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42DA05B8-1490-45B6-B22D-95176EBE7150">RegisterStereoStatusWindow</a>
</td>
<td align="left" width="63%">
Registers an application window to receive notification messages of changes of stereo status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/754A627C-0365-4AF5-A6DF-A8D646254ECF">UnregisterOcclusionStatus</a>
</td>
<td align="left" width="63%">
Unregisters a window or an event to stop it from receiving notification when occlusion status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E3994C4-DA37-4D17-9F4D-C31E48CDE170">UnregisterStereoStatus</a>
</td>
<td align="left" width="63%">
Unregisters a window or an event to stop it from receiving notification when stereo status changes.

</td>
</tr>
</table> 


## -remarks



To create a Microsoft DirectX Graphics Infrastructure (DXGI) 1.2 factory interface, pass <b>IDXGIFactory2</b> into either the <a href="https://msdn.microsoft.com/5d8fb726-b2dc-4326-a7ad-8324af3924de">CreateDXGIFactory</a> or <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a> function or call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from a factory object that either <b>CreateDXGIFactory</b> or <b>CreateDXGIFactory1</b> returns.


Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
You can request the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>, <a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>, or  <a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a> interface from the Direct3D device and then use the <a href="https://msdn.microsoft.com/7e7f7494-445e-4bf1-8b94-fc40b7d9b887">IDXGIObject::GetParent</a> method to locate 
the factory.  The following code shows how.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIDevice2 * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice2), (void **)&amp;pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice-&gt;GetParent(__uuidof(IDXGIAdapter), (void **)&amp;pDXGIAdapter);

IDXGIFactory2 * pIDXGIFactory;
pDXGIAdapter-&gt;GetParent(__uuidof(IDXGIFactory2), (void **)&amp;pIDXGIFactory);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>
 

 

