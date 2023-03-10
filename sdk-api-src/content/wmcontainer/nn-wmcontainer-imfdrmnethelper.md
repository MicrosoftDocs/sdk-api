---
UID: NN:wmcontainer.IMFDRMNetHelper
title: IMFDRMNetHelper (wmcontainer.h)
description: Configures Windows Media Digital Rights Management (DRM) for Network Devices on a network sink.
helpviewer_keywords: ["IMFDRMNetHelper","IMFDRMNetHelper interface [Media Foundation]","IMFDRMNetHelper interface [Media Foundation]","described","mf.imfdrmnethelper","wmcontainer/IMFDRMNetHelper"]
old-location: mf\imfdrmnethelper.htm
tech.root: mf
ms.assetid: 6f4ac19a-0972-4152-a64c-6c719efb396c
ms.date: 12/05/2018
ms.keywords: IMFDRMNetHelper, IMFDRMNetHelper interface [Media Foundation], IMFDRMNetHelper interface [Media Foundation],described, mf.imfdrmnethelper, wmcontainer/IMFDRMNetHelper
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDRMNetHelper
 - wmcontainer/IMFDRMNetHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcontainer.h
api_name:
 - IMFDRMNetHelper
---

# IMFDRMNetHelper interface


## -description

Configures Windows Media Digital Rights Management (DRM) for Network Devices on a network sink.

 The Advanced Systems Format (ASF) streaming media sink exposes this interface. To get a pointer to the <b>IMFDRMNetHelper</b> interface, perform the following tasks.
<ol>
<li>Get the activation object for the ASF streaming media sink by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfstreamingmediasinkactivate">MFCreateASFStreamingMediaSinkActivate</a>.</li>
<li>Create the media sink by calling  the activation object <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a> method.</li>
<li>Get an <b>IMFDRMNetHelper</b> pointer by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the media sink.</li>
</ol>For more information, see Remarks.

## -inheritance

The <b>IMFDRMNetHelper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDRMNetHelper</b> also has these types of members:

## -remarks

To stream protected content over a network, the <i>ASF streaming media sink</i> provides an output trust authority (OTA) that supports  Windows Media DRM for Network Devices and implements the <b>IMFDRMNetHelper</b> interface. For this OTA,  encryption occurs on each frame before multiplexing. The license request and response process takes place in the media sink.

The application gets a pointer to <b>IMFDRMNetHelper</b> and uses the methods to handle the license request and response. The application is also responsible for sending the license to the client.

To stream the content, the application does the following:

<ol>
<li>Provide the HTTP byte stream to which the media sink writes the streamed content. To stream DRM-protected content over a network from a server to a client, an application must use the Microsoft Media Foundation Protected Media Path (PMP). The media sink and the application-provided HTTP byte stream exist in  mfpmp.exe. Therefore, the byte stream must expose the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface so that it can be created out-of-process.<div class="alert"><b>Note</b>  This might affect how the code is packaged. The DLL that contains the HTTP byte stream and other dependent DLLs must be signed for the Protected Environment (PE-signed).  </div>
<div> </div>


</li>
<li>Set the <a href="/windows/desktop/medfound/mfpkey-asfmediasink-drmaction-property">MFPKEY_ASFMEDIASINK_DRMACTION</a> property to <b>MFSINK_WMDRMACTION_TRANSCRYPT</b>. The media sink's property store is available to the application through the <a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo</a>. To get the property store, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore">IMFASFContentInfo::GetEncodingConfigurationPropertyStore</a>.</li>
<li>Get a pointer to the <b>IMFDRMNetHelper</b> interface by querying the media sink.</li>
<li>To make a license request, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfdrmnethelper-processlicenserequest">IMFDRMNetHelper::ProcessLicenseRequest</a>. This method calls into the OTA implementation and retrieves the license.When the clock starts for the first time or restarts , the encrypter that is used for encrypting samples is retrieved, and   the license response is cached.

</li>
<li>To get the cached license response, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfdrmnethelper-getchainedlicenseresponse">IMFDRMNetHelper::GetChainedLicenseResponse</a>.</li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
