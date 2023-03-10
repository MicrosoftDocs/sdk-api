---
UID: NF:hrtfapoapi.IXAPOHrtfParameters.SetEnvironment
title: IXAPOHrtfParameters::SetEnvironment (hrtfapoapi.h)
description: Selects the acoustic environment to simulate.
helpviewer_keywords: ["IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs]","SetEnvironment method","IXAPOHrtfParameters.SetEnvironment","IXAPOHrtfParameters::SetEnvironment","SetEnvironment","SetEnvironment method [XAudio2 Audio Mixing APIs]","SetEnvironment method [XAudio2 Audio Mixing APIs]","IXAPOHrtfParameters interface","hrtfapoapi/IXAPOHrtfParameters::SetEnvironment","xaudio2.ixapohrtfparameters_setenvironment"]
old-location: xaudio2\ixapohrtfparameters_setenvironment.htm
tech.root: xaudio2
ms.assetid: 1AB999FB-E24C-4CC6-A3B9-D4F61FF31760
ms.date: 12/05/2018
ms.keywords: IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs],SetEnvironment method, IXAPOHrtfParameters.SetEnvironment, IXAPOHrtfParameters::SetEnvironment, SetEnvironment, SetEnvironment method [XAudio2 Audio Mixing APIs], SetEnvironment method [XAudio2 Audio Mixing APIs],IXAPOHrtfParameters interface, hrtfapoapi/IXAPOHrtfParameters::SetEnvironment, xaudio2.ixapohrtfparameters_setenvironment
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
 - IXAPOHrtfParameters::SetEnvironment
 - hrtfapoapi/IXAPOHrtfParameters::SetEnvironment
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
 - IXAPOHrtfParameters.SetEnvironment
---

# IXAPOHrtfParameters::SetEnvironment


## -description

Selects the acoustic environment to simulate.

## -parameters

### -param environment [in]

The acoustic environment to simulate.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The environment represents distance-cue params.

## -see-also

<a href="/windows/desktop/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters">IXAPOHrtfParameters</a>