---
UID: NN:wmcontainer.IMFDRMNetHelper
title: IMFDRMNetHelper
author: windows-driver-content
description: Configures Windows Media Digital Rights Management (DRM) for Network Devices on a network sink.
old-location: mf\imfdrmnethelper.htm
old-project: medfound
ms.assetid: 6f4ac19a-0972-4152-a64c-6c719efb396c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFDRMNetHelper, IMFDRMNetHelper interface [Media Foundation], IMFDRMNetHelper interface [Media Foundation],described, mf.imfdrmnethelper, wmcontainer/IMFDRMNetHelper
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmcontainer.h
api_name:
-	IMFDRMNetHelper
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFDRMNetHelper interface


## -description


Configures Windows Media Digital Rights Management (DRM) for Network Devices on a network sink.

 The Advanced Systems Format (ASF) streaming media sink exposes this interface. To get a pointer to the <b>IMFDRMNetHelper</b> interface, perform the following tasks.
<ol>
<li>Get the activation object for the ASF streaming media sink by calling <a href="https://msdn.microsoft.com/ffcab5ee-400a-424f-ab98-3c9e36ef40ce">MFCreateASFStreamingMediaSinkActivate</a>.</li>
<li>Create the media sink by calling  the activation object <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a> method.</li>
<li>Get an <b>IMFDRMNetHelper</b> pointer by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the media sink.</li>
</ol>For more information, see Remarks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDRMNetHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDRMNetHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDRMNetHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eedbefd8-8540-4bf9-b602-6bebf089fcf7">GetChainedLicenseResponse</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e60f9831-f59d-46ff-b685-b26d6484a70d">ProcessLicenseRequest</a>
</td>
<td align="left" width="63%">
Gets the license response for the specified request.

</td>
</tr>
</table> 


## -remarks



To stream protected content over a network, the <i>ASF streaming media sink</i> provides an output trust authority (OTA) that supports  Windows Media DRM for Network Devices and implements the <b>IMFDRMNetHelper</b> interface. For this OTA,  encryption occurs on each frame before multiplexing. The license request and response process takes place in the media sink.

The application gets a pointer to <b>IMFDRMNetHelper</b> and uses the methods to handle the license request and response. The application is also responsible for sending the license to the client.

To stream the content, the application does the following:

<ol>
<li>Provide the HTTP byte stream to which the media sink writes the streamed content. To stream DRM-protected content over a network from a server to a client, an application must use the Microsoft Media Foundation Protected Media Path (PMP). The media sink and the application-provided HTTP byte stream exist in  mfpmp.exe. Therefore, the byte stream must expose the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface so that it can be created out-of-process.<div class="alert"><b>Note</b>  This might affect how the code is packaged. The DLL that contains the HTTP byte stream and other dependent DLLs must be signed for the Protected Environment (PE-signed).  </div>
<div> </div>


</li>
<li>Set the <a href="https://msdn.microsoft.com/5f81294b-859a-4325-98dd-6267c736e1f1">MFPKEY_ASFMEDIASINK_DRMACTION</a> property to <b>MFSINK_WMDRMACTION_TRANSCRYPT</b>. The media sink's property store is available to the application through the <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo</a>. To get the property store, call <a href="https://msdn.microsoft.com/e77a5564-82bc-4c1d-9fb8-84ab484c4ca8">IMFASFContentInfo::GetEncodingConfigurationPropertyStore</a>.</li>
<li>Get a pointer to the <b>IMFDRMNetHelper</b> interface by querying the media sink.</li>
<li>To make a license request, call <a href="https://msdn.microsoft.com/e60f9831-f59d-46ff-b685-b26d6484a70d">IMFDRMNetHelper::ProcessLicenseRequest</a>. This method calls into the OTA implementation and retrieves the license.When the clock starts for the first time or restarts , the encrypter that is used for encrypting samples is retrieved, and   the license response is cached.

</li>
<li>To get the cached license response, call <a href="https://msdn.microsoft.com/eedbefd8-8540-4bf9-b602-6bebf089fcf7">IMFDRMNetHelper::GetChainedLicenseResponse</a>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

