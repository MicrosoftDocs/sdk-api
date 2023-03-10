---
UID: NN:mfmediaengine.IMFMediaEngineOPMInfo
title: IMFMediaEngineOPMInfo (mfmediaengine.h)
description: Provides methods for getting information about the Output Protection Manager (OPM).
helpviewer_keywords: ["IMFMediaEngineOPMInfo","IMFMediaEngineOPMInfo interface [Media Foundation]","IMFMediaEngineOPMInfo interface [Media Foundation]","described","mf.imfmediaengineopminfo","mfmediaengine/IMFMediaEngineOPMInfo"]
old-location: mf\imfmediaengineopminfo.htm
tech.root: mf
ms.assetid: 399f81ac-38f8-4aaa-8b34-f5fd13b71402
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineOPMInfo, IMFMediaEngineOPMInfo interface [Media Foundation], IMFMediaEngineOPMInfo interface [Media Foundation],described, mf.imfmediaengineopminfo, mfmediaengine/IMFMediaEngineOPMInfo
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaEngineOPMInfo
 - mfmediaengine/IMFMediaEngineOPMInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineOPMInfo
---

# IMFMediaEngineOPMInfo interface


## -description

Provides methods for getting information about the   <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM).

## -inheritance

The <b>IMFMediaEngineOPMInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineOPMInfo</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the Media Engine.

The <b>MF_MEDIA_ENGINE_EVENT_OPMINFO</b> <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> event is raised when there is a change in the OPM status.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
