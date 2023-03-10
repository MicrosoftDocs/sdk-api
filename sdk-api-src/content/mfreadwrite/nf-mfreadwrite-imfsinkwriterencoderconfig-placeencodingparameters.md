---
UID: NF:mfreadwrite.IMFSinkWriterEncoderConfig.PlaceEncodingParameters
title: IMFSinkWriterEncoderConfig::PlaceEncodingParameters (mfreadwrite.h)
description: Dynamically updates the encoder configuration with a collection of new encoder settings.
helpviewer_keywords: ["IMFSinkWriterEncoderConfig interface [Media Foundation]","PlaceEncodingParameters method","IMFSinkWriterEncoderConfig.PlaceEncodingParameters","IMFSinkWriterEncoderConfig::PlaceEncodingParameters","PlaceEncodingParameters","PlaceEncodingParameters method [Media Foundation]","PlaceEncodingParameters method [Media Foundation]","IMFSinkWriterEncoderConfig interface","mf.imfsinkwriterencoderconfig_placeencodingparameters","mfreadwrite/IMFSinkWriterEncoderConfig::PlaceEncodingParameters"]
old-location: mf\imfsinkwriterencoderconfig_placeencodingparameters.htm
tech.root: mf
ms.assetid: ea09d806-c869-4a62-8f9d-c35db4e406ff
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterEncoderConfig interface [Media Foundation],PlaceEncodingParameters method, IMFSinkWriterEncoderConfig.PlaceEncodingParameters, IMFSinkWriterEncoderConfig::PlaceEncodingParameters, PlaceEncodingParameters, PlaceEncodingParameters method [Media Foundation], PlaceEncodingParameters method [Media Foundation],IMFSinkWriterEncoderConfig interface, mf.imfsinkwriterencoderconfig_placeencodingparameters, mfreadwrite/IMFSinkWriterEncoderConfig::PlaceEncodingParameters
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfreadwrite.idl
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
 - IMFSinkWriterEncoderConfig::PlaceEncodingParameters
 - mfreadwrite/IMFSinkWriterEncoderConfig::PlaceEncodingParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriterEncoderConfig.PlaceEncodingParameters
---

# IMFSinkWriterEncoderConfig::PlaceEncodingParameters


## -description

Dynamically updates the encoder configuration with a collection of new encoder settings.

## -parameters

### -param dwStreamIndex [in]

Specifies the stream index.

### -param pEncodingParameters [in]

A set of encoding parameters to configure the encoder with.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The encoder will be configured with these settings after all previously queued input media samples have been sent to it through <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput">IMFTransform::ProcessInput</a>.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig">IMFSinkWriterEncoderConfig</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>