---
UID: NN:mfidl.IMFPMPHost
title: IMFPMPHost (mfidl.h)
description: Enables a media source in the application process to create objects in the protected media path (PMP) process.
helpviewer_keywords: ["IMFPMPHost","IMFPMPHost interface [Media Foundation]","IMFPMPHost interface [Media Foundation]","described","fab1fb42-07c5-4a74-b6f5-0950b2c3ba46","mf.imfpmphost","mfidl/IMFPMPHost"]
old-location: mf\imfpmphost.htm
tech.root: mf
ms.assetid: fab1fb42-07c5-4a74-b6f5-0950b2c3ba46
ms.date: 12/05/2018
ms.keywords: IMFPMPHost, IMFPMPHost interface [Media Foundation], IMFPMPHost interface [Media Foundation],described, fab1fb42-07c5-4a74-b6f5-0950b2c3ba46, mf.imfpmphost, mfidl/IMFPMPHost
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPHost
 - mfidl/IMFPMPHost
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPHost
---

# IMFPMPHost interface


## -description

Enables a media source in the application process to create objects in the protected media path (PMP) process.

## -inheritance

The <b>IMFPMPHost</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPHost</b> also has these types of members:

## -remarks

This interface is used when a media source resides in the application process but the Media Session resides in a PMP process. The media source can use this interface to create objects in the PMP process. For example, to play DRM-protected content, the media source typically must create an input trust authority (ITA) in the PMP process. 

To use this interface, the media source implements the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient">IMFPMPClient</a> interface. The PMP Media Session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost">IMFPMPClient::SetPMPHost</a> on the media source, passing in a pointer to the <b>IMFPMPHost</b> interface.

You can also get a pointer to this interface by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the PMP Media Session, using the service identifier <b>MF_PMP_SERVICE</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
