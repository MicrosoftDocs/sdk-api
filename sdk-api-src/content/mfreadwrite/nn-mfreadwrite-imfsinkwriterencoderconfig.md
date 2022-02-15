---
UID: NN:mfreadwrite.IMFSinkWriterEncoderConfig
title: IMFSinkWriterEncoderConfig (mfreadwrite.h)
description: Provides additional functionality on the sink writer for dynamically changing the media type and encoder configuration.
helpviewer_keywords: ["IMFSinkWriterEncoderConfig","IMFSinkWriterEncoderConfig interface [Media Foundation]","IMFSinkWriterEncoderConfig interface [Media Foundation]","described","mf.imfsinkwriterencoderconfig","mfreadwrite/IMFSinkWriterEncoderConfig"]
old-location: mf\imfsinkwriterencoderconfig.htm
tech.root: mf
ms.assetid: 3a0d090d-9eb1-4624-989b-c5da27b988aa
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterEncoderConfig, IMFSinkWriterEncoderConfig interface [Media Foundation], IMFSinkWriterEncoderConfig interface [Media Foundation],described, mf.imfsinkwriterencoderconfig, mfreadwrite/IMFSinkWriterEncoderConfig
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
 - IMFSinkWriterEncoderConfig
 - mfreadwrite/IMFSinkWriterEncoderConfig
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
 - IMFSinkWriterEncoderConfig
---

# IMFSinkWriterEncoderConfig interface


## -description

Provides additional functionality on the sink writer for dynamically changing the media type and encoder configuration.

## -inheritance

The <b>IMFSinkWriterEncoderConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterEncoderConfig</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/medfound/sink-writer">Sink Writer</a> implements this interface in Windows 8.1. To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
