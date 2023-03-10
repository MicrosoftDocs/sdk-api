---
UID: NF:hrtfapoapi.IXAPOHrtfParameters.SetSourceGain
title: IXAPOHrtfParameters::SetSourceGain (hrtfapoapi.h)
description: Sets the custom direct-path gain value for the current source position. Valid only for sounds played with the HrtfDistanceDecayType custom decay type.
helpviewer_keywords: ["IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs]","SetSourceGain method","IXAPOHrtfParameters.SetSourceGain","IXAPOHrtfParameters::SetSourceGain","SetSourceGain","SetSourceGain method [XAudio2 Audio Mixing APIs]","SetSourceGain method [XAudio2 Audio Mixing APIs]","IXAPOHrtfParameters interface","hrtfapoapi/IXAPOHrtfParameters::SetSourceGain","xaudio2.ixapohrtfparameters_setsourcegain"]
old-location: xaudio2\ixapohrtfparameters_setsourcegain.htm
tech.root: xaudio2
ms.assetid: B1060FF1-6E0F-4B09-BB1B-2517933676D1
ms.date: 12/05/2018
ms.keywords: IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs],SetSourceGain method, IXAPOHrtfParameters.SetSourceGain, IXAPOHrtfParameters::SetSourceGain, SetSourceGain, SetSourceGain method [XAudio2 Audio Mixing APIs], SetSourceGain method [XAudio2 Audio Mixing APIs],IXAPOHrtfParameters interface, hrtfapoapi/IXAPOHrtfParameters::SetSourceGain, xaudio2.ixapohrtfparameters_setsourcegain
req.header: hrtfapoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: HrtfApo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPOHrtfParameters::SetSourceGain
 - hrtfapoapi/IXAPOHrtfParameters::SetSourceGain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - HrtfApo.dll
api_name:
 - IXAPOHrtfParameters.SetSourceGain
---

# IXAPOHrtfParameters::SetSourceGain


## -description

Sets the custom direct-path gain value for the current source position in dB. Valid only for sounds played with the HrtfDistanceDecayType custom decay type.

## -parameters

### -param gain [in]

The custom direct-path gain value for the current source position in dB. Valid only for sounds played with the HrtfDistanceDecayType custom decay type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters">IXAPOHrtfParameters</a>