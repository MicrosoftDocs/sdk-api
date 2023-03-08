---
UID: NN:mfidl.IMFMediaSourcePresentationProvider
title: IMFMediaSourcePresentationProvider (mfidl.h)
description: Provides notifications to the sequencer source.
helpviewer_keywords: ["IMFMediaSourcePresentationProvider","IMFMediaSourcePresentationProvider interface [Media Foundation]","IMFMediaSourcePresentationProvider interface [Media Foundation]","described","b6b36324-a315-42a0-bdbf-8d2cec6cde3f","mf.imfmediasourcepresentationprovider","mfidl/IMFMediaSourcePresentationProvider"]
old-location: mf\imfmediasourcepresentationprovider.htm
tech.root: mf
ms.assetid: b6b36324-a315-42a0-bdbf-8d2cec6cde3f
ms.date: 12/05/2018
ms.keywords: IMFMediaSourcePresentationProvider, IMFMediaSourcePresentationProvider interface [Media Foundation], IMFMediaSourcePresentationProvider interface [Media Foundation],described, b6b36324-a315-42a0-bdbf-8d2cec6cde3f, mf.imfmediasourcepresentationprovider, mfidl/IMFMediaSourcePresentationProvider
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
 - IMFMediaSourcePresentationProvider
 - mfidl/IMFMediaSourcePresentationProvider
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
 - IMFMediaSourcePresentationProvider
---

# IMFMediaSourcePresentationProvider interface


## -description

Provides notifications to the sequencer source. This interface is exposed by the sequencer source. Applications do not use this interface.

To get a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_SOURCE_PRESENTATION_PROVIDER_SERVICE.

## -inheritance

The <b>IMFMediaSourcePresentationProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSourcePresentationProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
