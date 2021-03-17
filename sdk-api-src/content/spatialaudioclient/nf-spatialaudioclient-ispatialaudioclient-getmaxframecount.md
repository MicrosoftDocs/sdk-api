---
UID: NF:spatialaudioclient.ISpatialAudioClient.GetMaxFrameCount
title: ISpatialAudioClient::GetMaxFrameCount (spatialaudioclient.h)
description: Gets the maximum possible frame count per processing pass. This method can be used to determine the size of the source buffer that should be allocated to convey audio data for each processing pass.
helpviewer_keywords: ["GetMaxFrameCount","GetMaxFrameCount method [Core Audio]","GetMaxFrameCount method [Core Audio]","ISpatialAudioClient interface","ISpatialAudioClient interface [Core Audio]","GetMaxFrameCount method","ISpatialAudioClient.GetMaxFrameCount","ISpatialAudioClient::GetMaxFrameCount","coreaudio.ispatialaudioclient_getmaxframecount","spatialaudioclient/ISpatialAudioClient::GetMaxFrameCount"]
old-location: coreaudio\ispatialaudioclient_getmaxframecount.htm
tech.root: CoreAudio
ms.assetid: CA28103B-6C9C-46C8-9C21-73573B42DDC4
ms.date: 12/05/2018
ms.keywords: GetMaxFrameCount, GetMaxFrameCount method [Core Audio], GetMaxFrameCount method [Core Audio],ISpatialAudioClient interface, ISpatialAudioClient interface [Core Audio],GetMaxFrameCount method, ISpatialAudioClient.GetMaxFrameCount, ISpatialAudioClient::GetMaxFrameCount, coreaudio.ispatialaudioclient_getmaxframecount, spatialaudioclient/ISpatialAudioClient::GetMaxFrameCount
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISpatialAudioClient::GetMaxFrameCount
 - spatialaudioclient/ISpatialAudioClient::GetMaxFrameCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioClient.GetMaxFrameCount
---

# ISpatialAudioClient::GetMaxFrameCount


## -description

Gets the maximum possible frame count per processing pass. This method can be used to determine the size of the source buffer that should be allocated to convey audio data for each processing pass.

## -parameters

### -param objectFormat [in]

The audio format used to calculate the maximum frame count. This should be the same format specified in the <b>ObjectFormat</b> field of the <a href="/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams">SpatialAudioObjectRenderStreamActivationParams</a> passed to  <a href="/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream">ActivateSpatialAudioStream</a>.

### -param frameCountPerBuffer [out]

The maximum number of audio frames that will be processed in one pass.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient">ISpatialAudioClient</a>