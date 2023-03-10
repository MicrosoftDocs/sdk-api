---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetInBandMetadataTrackDispatchType
title: IMFTimedTextTrack::GetInBandMetadataTrackDispatchType (mfmediaengine.h)
description: Gets the in-band metadata of the track.
helpviewer_keywords: ["GetInBandMetadataTrackDispatchType","GetInBandMetadataTrackDispatchType method [Media Foundation]","GetInBandMetadataTrackDispatchType method [Media Foundation]","IMFTimedTextTrack interface","IMFTimedTextTrack interface [Media Foundation]","GetInBandMetadataTrackDispatchType method","IMFTimedTextTrack.GetInBandMetadataTrackDispatchType","IMFTimedTextTrack::GetInBandMetadataTrackDispatchType","mf.imftimedtexttrack_getinbandmetadatatrackdispatchtype","mfmediaengine/IMFTimedTextTrack::GetInBandMetadataTrackDispatchType"]
old-location: mf\imftimedtexttrack_getinbandmetadatatrackdispatchtype.htm
tech.root: mf
ms.assetid: AEA4D160-6DBC-4829-95F3-F016F9709042
ms.date: 12/05/2018
ms.keywords: GetInBandMetadataTrackDispatchType, GetInBandMetadataTrackDispatchType method [Media Foundation], GetInBandMetadataTrackDispatchType method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetInBandMetadataTrackDispatchType method, IMFTimedTextTrack.GetInBandMetadataTrackDispatchType, IMFTimedTextTrack::GetInBandMetadataTrackDispatchType, mf.imftimedtexttrack_getinbandmetadatatrackdispatchtype, mfmediaengine/IMFTimedTextTrack::GetInBandMetadataTrackDispatchType
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IMFTimedTextTrack::GetInBandMetadataTrackDispatchType
 - mfmediaengine/IMFTimedTextTrack::GetInBandMetadataTrackDispatchType
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
 - IMFTimedTextTrack.GetInBandMetadataTrackDispatchType
---

# IMFTimedTextTrack::GetInBandMetadataTrackDispatchType


## -description

Gets the in-band metadata of the track.

## -parameters

### -param dispatchType [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the in-band metadata of the track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>