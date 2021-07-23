---
UID: NF:hrtfapoapi.IXAPOHrtfParameters.SetSourceOrientation
title: IXAPOHrtfParameters::SetSourceOrientation (hrtfapoapi.h)
description: Set the rotation matrix for the source orientation, with respect to the listener's coordinate system.
helpviewer_keywords: ["IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs]","SetSourceOrientation method","IXAPOHrtfParameters.SetSourceOrientation","IXAPOHrtfParameters::SetSourceOrientation","SetSourceOrientation","SetSourceOrientation method [XAudio2 Audio Mixing APIs]","SetSourceOrientation method [XAudio2 Audio Mixing APIs]","IXAPOHrtfParameters interface","hrtfapoapi/IXAPOHrtfParameters::SetSourceOrientation","xaudio2.ixapohrtfparameters_setsourceorientation"]
old-location: xaudio2\ixapohrtfparameters_setsourceorientation.htm
tech.root: xaudio2
ms.assetid: 5E2F0A64-39BB-47B6-8C64-1FDB0B5C537C
ms.date: 12/05/2018
ms.keywords: IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs],SetSourceOrientation method, IXAPOHrtfParameters.SetSourceOrientation, IXAPOHrtfParameters::SetSourceOrientation, SetSourceOrientation, SetSourceOrientation method [XAudio2 Audio Mixing APIs], SetSourceOrientation method [XAudio2 Audio Mixing APIs],IXAPOHrtfParameters interface, hrtfapoapi/IXAPOHrtfParameters::SetSourceOrientation, xaudio2.ixapohrtfparameters_setsourceorientation
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
 - IXAPOHrtfParameters::SetSourceOrientation
 - hrtfapoapi/IXAPOHrtfParameters::SetSourceOrientation
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
 - IXAPOHrtfParameters.SetSourceOrientation
---

# IXAPOHrtfParameters::SetSourceOrientation


## -description

Set the rotation matrix for the source orientation, with respect to the listener's coordinate system.

## -parameters

### -param orientation [in]

The rotation matrix for the source orientation, with respect to the listener's frame of reference.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters">IXAPOHrtfParameters</a>