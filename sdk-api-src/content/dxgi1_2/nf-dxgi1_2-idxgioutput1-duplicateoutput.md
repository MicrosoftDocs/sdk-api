---
UID: NF:dxgi1_2.IDXGIOutput1.DuplicateOutput
title: IDXGIOutput1::DuplicateOutput
author: windows-sdk-content
description: Creates a desktop duplication interface from the IDXGIOutput1 interface that represents an adapter output.
old-location: direct3ddxgi\idxgioutput1_duplicateoutput.htm
old-project: direct3ddxgi
ms.assetid: 32B13906-0920-4891-B1E7-BCB291E78E73
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: DuplicateOutput, DuplicateOutput method [DXGI], DuplicateOutput method [DXGI],IDXGIOutput1 interface, IDXGIOutput1 interface [DXGI],DuplicateOutput method, IDXGIOutput1.DuplicateOutput, IDXGIOutput1::DuplicateOutput, direct3ddxgi.idxgioutput1_duplicateoutput, dxgi1_2/IDXGIOutput1::DuplicateOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
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
 - IDXGIOutput1.DuplicateOutput
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput1::DuplicateOutput


## -description


Creates a desktop duplication interface from the <a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a> interface that represents an adapter output.


## -parameters




### -param pDevice [in]

A pointer to the Direct3D device interface that you can use to process the desktop image. This device must be created from the adapter to which the output is connected.


### -param ppOutputDuplication [out]

A pointer to a variable that receives the new <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface.


## -returns



<b>DuplicateOutput</b> returns:
        <ul>
<li>S_OK if <b>DuplicateOutput</b> successfully created the desktop duplication interface.</li>
<li>E_INVALIDARG for one of the following reasons: <ul>
<li>The specified device (<i>pDevice</i>) is invalid, was not created on the correct adapter, or was not created from <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> (or a later version of a DXGI factory interface that inherits from <b>IDXGIFactory1</b>).</li>
<li>The calling application is already duplicating this desktop output.</li>
</ul>
</li>
<li>E_ACCESSDENIED if the application does not have access privilege  to the current desktop image.  For example, only an application that runs at LOCAL_SYSTEM can access the secure desktop.</li>
<li>DXGI_ERROR_UNSUPPORTED if the created <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface does not support the current desktop mode or scenario.  For example, 8bpp and non-DWM desktop modes are not supported. If <b>DuplicateOutput</b> fails with DXGI_ERROR_UNSUPPORTED, the application can wait for system notification of desktop switches and mode changes and then call <b>DuplicateOutput</b> again after such a notification occurs.  For more information, refer to <a href="https://msdn.microsoft.com/e27b135d-4faf-401e-a6c1-64ed0e1b5de5">EVENT_SYSTEM_DESKTOPSWITCH</a> and mode change notification (<a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a>). </li>
<li>DXGI_ERROR_NOT_CURRENTLY_AVAILABLE if DXGI reached the limit on the maximum number of concurrent duplication applications (default of four). Therefore, the calling application cannot create any desktop duplication interfaces until the other applications close.</li>
<li>DXGI_ERROR_SESSION_DISCONNECTED if <b>DuplicateOutput</b> failed because the session is currently disconnected.</li>
<li>Other error codes are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>DuplicateOutput</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



If an application wants to duplicate the entire desktop, it must create a desktop duplication interface on each active output on the desktop. This interface does not provide an explicit way to synchronize the timing of each output image. Instead, the application must use the time stamp of each output, and then determine how to combine the images.

For <b>DuplicateOutput</b> to succeed, you must create <i>pDevice</i> from <a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a> or a later version of a DXGI factory interface that inherits from <b>IDXGIFactory1</b>.

If the current mode is a stereo mode, the desktop duplication interface provides the image for the left stereo image only.

By default, only four processes can use a <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface at the same time within a single session. A process can have only one desktop duplication interface on a single desktop output; however, that process can have a desktop duplication interface for each output that is part of the desktop. 

For improved performance, consider using <a href="https://msdn.microsoft.com/B6723F05-E0D9-4814-8AB8-796ECF9C5C0C">DuplicateOutput1</a>.




## -see-also




<a href="https://msdn.microsoft.com/B6723F05-E0D9-4814-8AB8-796ECF9C5C0C">DuplicateOutput1</a>



<a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a>
 

 

