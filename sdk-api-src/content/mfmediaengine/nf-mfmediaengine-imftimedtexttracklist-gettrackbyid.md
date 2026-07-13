---
UID: NF:mfmediaengine.IMFTimedTextTrackList.GetTrackById
title: IMFTimedTextTrackList::GetTrackById (mfmediaengine.h)
description: Gets a text track in the list from the identifier of the track.
helpviewer_keywords: ["GetTrackById","GetTrackById method [Media Foundation]","GetTrackById method [Media Foundation]","IMFTimedTextTrackList interface","IMFTimedTextTrackList interface [Media Foundation]","GetTrackById method","IMFTimedTextTrackList.GetTrackById","IMFTimedTextTrackList::GetTrackById","mf.imftimedtexttracklist_gettrackbyid","mfmediaengine/IMFTimedTextTrackList::GetTrackById"]
old-location: mf\imftimedtexttracklist_gettrackbyid.htm
tech.root: mf
ms.assetid: 5653ED8A-36B1-488C-9D76-50D64BA78BA8
ms.date: 12/05/2018
ms.keywords: GetTrackById, GetTrackById method [Media Foundation], GetTrackById method [Media Foundation],IMFTimedTextTrackList interface, IMFTimedTextTrackList interface [Media Foundation],GetTrackById method, IMFTimedTextTrackList.GetTrackById, IMFTimedTextTrackList::GetTrackById, mf.imftimedtexttracklist_gettrackbyid, mfmediaengine/IMFTimedTextTrackList::GetTrackById
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
 - IMFTimedTextTrackList::GetTrackById
 - mfmediaengine/IMFTimedTextTrackList::GetTrackById
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
 - IMFTimedTextTrackList.GetTrackById
---

# IMFTimedTextTrackList::GetTrackById


## -description

Gets a text track in the list from the identifier of the track.

## -parameters

### -param trackId [in]

Type: <b>DWORD</b>

The identifier of the track in the list to retrieve.

### -param track [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a> interface for the timed-text track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>