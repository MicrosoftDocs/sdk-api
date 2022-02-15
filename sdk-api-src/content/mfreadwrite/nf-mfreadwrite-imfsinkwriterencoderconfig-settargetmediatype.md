---
UID: NF:mfreadwrite.IMFSinkWriterEncoderConfig.SetTargetMediaType
title: IMFSinkWriterEncoderConfig::SetTargetMediaType (mfreadwrite.h)
description: Dynamically changes the target media type that Sink Writer is encoding to.
helpviewer_keywords: ["IMFSinkWriterEncoderConfig interface [Media Foundation]","SetTargetMediaType method","IMFSinkWriterEncoderConfig.SetTargetMediaType","IMFSinkWriterEncoderConfig::SetTargetMediaType","SetTargetMediaType","SetTargetMediaType method [Media Foundation]","SetTargetMediaType method [Media Foundation]","IMFSinkWriterEncoderConfig interface","mf.imfsinkwriterencoderconfig_settargetmediatype","mfreadwrite/IMFSinkWriterEncoderConfig::SetTargetMediaType"]
old-location: mf\imfsinkwriterencoderconfig_settargetmediatype.htm
tech.root: mf
ms.assetid: 26d6ee83-5899-40e7-8b71-ca47f5b0d1c1
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterEncoderConfig interface [Media Foundation],SetTargetMediaType method, IMFSinkWriterEncoderConfig.SetTargetMediaType, IMFSinkWriterEncoderConfig::SetTargetMediaType, SetTargetMediaType, SetTargetMediaType method [Media Foundation], SetTargetMediaType method [Media Foundation],IMFSinkWriterEncoderConfig interface, mf.imfsinkwriterencoderconfig_settargetmediatype, mfreadwrite/IMFSinkWriterEncoderConfig::SetTargetMediaType
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
 - IMFSinkWriterEncoderConfig::SetTargetMediaType
 - mfreadwrite/IMFSinkWriterEncoderConfig::SetTargetMediaType
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
 - IMFSinkWriterEncoderConfig.SetTargetMediaType
---

# IMFSinkWriterEncoderConfig::SetTargetMediaType


## -description

Dynamically changes the target media type that Sink Writer is encoding to.

## -parameters

### -param dwStreamIndex [in]

Specifies the stream index.

### -param pTargetMediaType [in]

The new media format to encode to.

### -param pEncodingParameters [in]

The new set of encoding parameters to configure the encoder with.
    If not specified, previously provided parameters will be used.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The new media type must be supported by the media sink being used and by     the encoder MFTs installed on the system.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig">IMFSinkWriterEncoderConfig</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>