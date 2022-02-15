---
UID: NN:mfidl.IMFAudioPolicy
title: IMFAudioPolicy (mfidl.h)
description: Configures the audio session that is associated with the streaming audio renderer (SAR).
helpviewer_keywords: ["IMFAudioPolicy","IMFAudioPolicy interface [Media Foundation]","IMFAudioPolicy interface [Media Foundation]","described","fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a","mf.imfaudiopolicy","mfidl/IMFAudioPolicy"]
old-location: mf\imfaudiopolicy.htm
tech.root: mf
ms.assetid: fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a
ms.date: 12/05/2018
ms.keywords: IMFAudioPolicy, IMFAudioPolicy interface [Media Foundation], IMFAudioPolicy interface [Media Foundation],described, fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a, mf.imfaudiopolicy, mfidl/IMFAudioPolicy
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
 - IMFAudioPolicy
 - mfidl/IMFAudioPolicy
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
 - IMFAudioPolicy
---

# IMFAudioPolicy interface


## -description

Configures the audio session that is associated with the streaming audio renderer (SAR). Use this interface to change how the audio session appears in the Windows volume control.

The SAR exposes this interface as a service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MR_AUDIO_POLICY_SERVICE. You can call <b>GetService</b> directly on the SAR or call it on the Media Session.

## -inheritance

The <b>IMFAudioPolicy</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAudioPolicy</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
