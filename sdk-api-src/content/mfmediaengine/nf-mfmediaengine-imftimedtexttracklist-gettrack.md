---
UID: NF:mfmediaengine.IMFTimedTextTrackList.GetTrack
title: IMFTimedTextTrackList::GetTrack (mfmediaengine.h)
description: Gets a text track in the list from the index of the track.
helpviewer_keywords: ["GetTrack","GetTrack method [Media Foundation]","GetTrack method [Media Foundation]","IMFTimedTextTrackList interface","IMFTimedTextTrackList interface [Media Foundation]","GetTrack method","IMFTimedTextTrackList.GetTrack","IMFTimedTextTrackList::GetTrack","mf.imftimedtexttracklist_gettrack","mfmediaengine/IMFTimedTextTrackList::GetTrack"]
old-location: mf\imftimedtexttracklist_gettrack.htm
tech.root: mf
ms.assetid: 5AF4F317-E46D-459A-900B-6D4796CD59A2
ms.date: 12/05/2018
ms.keywords: GetTrack, GetTrack method [Media Foundation], GetTrack method [Media Foundation],IMFTimedTextTrackList interface, IMFTimedTextTrackList interface [Media Foundation],GetTrack method, IMFTimedTextTrackList.GetTrack, IMFTimedTextTrackList::GetTrack, mf.imftimedtexttracklist_gettrack, mfmediaengine/IMFTimedTextTrackList::GetTrack
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
 - IMFTimedTextTrackList::GetTrack
 - mfmediaengine/IMFTimedTextTrackList::GetTrack
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
 - IMFTimedTextTrackList.GetTrack
---

# IMFTimedTextTrackList::GetTrack


## -description

Gets a text track in the list from the index of the track.

## -parameters

### -param index [in]

Type: <b>DWORD</b>

The index of the track in the list to retrieve.

### -param track [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a> interface for the timed-text track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>