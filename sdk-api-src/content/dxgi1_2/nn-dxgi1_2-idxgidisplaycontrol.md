---
UID: NN:dxgi1_2.IDXGIDisplayControl
title: IDXGIDisplayControl
author: windows-sdk-content
description: The IDXGIDisplayControl interface exposes methods to indicate user preference for the operating system's stereoscopic 3D display behavior and to set stereoscopic 3D display status to enable or disable.
old-location: direct3ddxgi\idxgidisplaycontrol.htm
old-project: direct3ddxgi
ms.assetid: 8E9A059E-D7E2-4179-9ECA-D66BC9CD3757
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDXGIDisplayControl, IDXGIDisplayControl interface [DXGI], IDXGIDisplayControl interface [DXGI],described, direct3ddxgi.idxgidisplaycontrol, dxgi1_2/IDXGIDisplayControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIDisplayControl
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDisplayControl interface


## -description



The <b>IDXGIDisplayControl</b> interface exposes methods to indicate user preference for the operating system's stereoscopic 3D display behavior and to set stereoscopic 3D display status to enable or disable.
        



We recommend that you not use <b>IDXGIDisplayControl</b> to query or set system-wide stereoscopic 3D settings in your stereoscopic 3D apps. Instead, for your windowed apps, call the <a href="https://msdn.microsoft.com/81DA1DD6-7D36-4848-ADCB-1F7B765B0A62">IDXGIFactory2::IsWindowedStereoEnabled</a> method to determine whether to render in stereo; for your full-screen apps, call the <a href="https://msdn.microsoft.com/49522ED9-30AD-4F39-96D2-BB6677D72349">IDXGIOutput1::GetDisplayModeList1</a> method and then determine whether any of the returned display modes support rendering in stereo.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDisplayControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIDisplayControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDisplayControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE6AA254-3534-4E0F-A206-BAC4536B8B80">IsStereoEnabled</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4A449444-287D-4F1D-9A86-F6165C38048F">SetStereoEnabled</a>
</td>
<td align="left" width="63%">
Set a Boolean value to either enable or disable the operating system's stereoscopic 3D display behavior.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  The <b>IDXGIDisplayControl</b> interface is only used by the <b>Display</b> app of the operating system's Control Panel or by control applets from third party graphics vendors. This interface is not meant for developers of end-user apps.
        </div>
<div> </div>
<div class="alert"><b>Note</b>  The <b>IDXGIDisplayControl</b> interface does not exist for Windows Store apps.
        </div>
<div> </div>
Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from a factory object (<a href="https://msdn.microsoft.com/642aac36-ca5a-4c62-b5cb-f9d35965ca2f">IDXGIFactory</a>, <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> or <a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>) to retrieve the <b>IDXGIDisplayControl</b> interface. The following code shows how.
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIDisplayControl * pDXGIDisplayControl;
hr = g_pDXGIFactory-&gt;QueryInterface(__uuidof(IDXGIDisplayControl), (void **)&amp;pDXGIDisplayControl);</pre>
</td>
</tr>
</table></span></div>
The operating system processes changes to stereo-enabled configuration asynchronously. Therefore, these changes might not be immediately visible in every process that calls <a href="https://msdn.microsoft.com/AE6AA254-3534-4E0F-A206-BAC4536B8B80">IDXGIDisplayControl::IsStereoEnabled</a> to query for stereo configuration.  Control applets can use the <a href="https://msdn.microsoft.com/912FC8B0-8B66-4203-BF27-8D7186F7CAC0">IDXGIFactory2::RegisterStereoStatusEvent</a> or <a href="https://msdn.microsoft.com/42DA05B8-1490-45B6-B22D-95176EBE7150">IDXGIFactory2::RegisterStereoStatusWindow</a> method to register for notifications of all stereo configuration changes.
        

<b>Platform Update for Windows 7:  </b>Stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

