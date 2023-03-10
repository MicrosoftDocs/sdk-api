---
UID: NN:mfidl.IMFMetadataProvider
title: IMFMetadataProvider (mfidl.h)
description: Gets metadata from a media source or other object.
helpviewer_keywords: ["IMFMetadataProvider","IMFMetadataProvider interface [Media Foundation]","IMFMetadataProvider interface [Media Foundation]","described","f32e78c9-a567-448d-947d-d7ea996bba5e","mf.imfmetadataprovider","mfidl/IMFMetadataProvider"]
old-location: mf\imfmetadataprovider.htm
tech.root: mf
ms.assetid: f32e78c9-a567-448d-947d-d7ea996bba5e
ms.date: 12/05/2018
ms.keywords: IMFMetadataProvider, IMFMetadataProvider interface [Media Foundation], IMFMetadataProvider interface [Media Foundation],described, f32e78c9-a567-448d-947d-d7ea996bba5e, mf.imfmetadataprovider, mfidl/IMFMetadataProvider
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFMetadataProvider
 - mfidl/IMFMetadataProvider
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
 - IMFMetadataProvider
---

# IMFMetadataProvider interface


## -description

Gets metadata from a media source or other object.

If a media source supports this interface, it must expose the interface as a service. To get a pointer to this interface from a media source, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is <b>MF_METADATA_PROVIDER_SERVICE</b>. Other types of object can expose this interface through <b>QueryInterface</b>.

Use this interface to get a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a> interface.

## -inheritance

The <b>IMFMetadataProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMetadataProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
