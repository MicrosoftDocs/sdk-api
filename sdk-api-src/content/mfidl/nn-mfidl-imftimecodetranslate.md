---
UID: NN:mfidl.IMFTimecodeTranslate
title: IMFTimecodeTranslate (mfidl.h)
description: Converts between Society of Motion Picture and Television Engineers (SMPTE) time codes and 100-nanosecond time units.
helpviewer_keywords: ["IMFTimecodeTranslate","IMFTimecodeTranslate interface [Media Foundation]","IMFTimecodeTranslate interface [Media Foundation]","described","mf.imftimecodetranslate","mfidl/IMFTimecodeTranslate"]
old-location: mf\imftimecodetranslate.htm
tech.root: mf
ms.assetid: 935ec6b3-12e6-4458-b8a1-ffeb4159d957
ms.date: 12/05/2018
ms.keywords: IMFTimecodeTranslate, IMFTimecodeTranslate interface [Media Foundation], IMFTimecodeTranslate interface [Media Foundation],described, mf.imftimecodetranslate, mfidl/IMFTimecodeTranslate
req.header: mfidl.h
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
 - IMFTimecodeTranslate
 - mfidl/IMFTimecodeTranslate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTimecodeTranslate
---

# IMFTimecodeTranslate interface


## -description

Converts between Society of Motion Picture and Television Engineers (SMPTE) time codes and 100-nanosecond time units.

## -inheritance

The <b>IMFTimecodeTranslate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimecodeTranslate</b> also has these types of members:

## -remarks

If an object supports this interface, it must expose the interface as a service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier <b>MF_TIMECODE_SERVICE</b>.

The Advanced Streaming Format (ASF) media source exposes this interface.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
