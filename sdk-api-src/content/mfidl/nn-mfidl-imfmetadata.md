---
UID: NN:mfidl.IMFMetadata
title: IMFMetadata (mfidl.h)
description: Manages metadata for an object.
helpviewer_keywords: ["411658ca-dc5e-445b-8d61-0c0429fcfbb1","IMFMetadata","IMFMetadata interface [Media Foundation]","IMFMetadata interface [Media Foundation]","described","mf.imfmetadata","mfidl/IMFMetadata"]
old-location: mf\imfmetadata.htm
tech.root: mf
ms.assetid: 411658ca-dc5e-445b-8d61-0c0429fcfbb1
ms.date: 12/05/2018
ms.keywords: 411658ca-dc5e-445b-8d61-0c0429fcfbb1, IMFMetadata, IMFMetadata interface [Media Foundation], IMFMetadata interface [Media Foundation],described, mf.imfmetadata, mfidl/IMFMetadata
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
 - IMFMetadata
 - mfidl/IMFMetadata
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
 - IMFMetadata
---

# IMFMetadata interface


## -description

Manages metadata for an object. Metadata is information that describes a media file, stream, or other content. Metadata consists of individual properties, where each property contains a descriptive name and a value. A property may be associated with a particular language.

To get this interface from a media source, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider">IMFMetadataProvider</a> interface.

## -inheritance

The <b>IMFMetadata</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMetadata</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider">IMFMetadataProvider</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>
