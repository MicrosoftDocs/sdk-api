---
UID: NF:mfmediaengine.IMFTimedTextTrackList.GetTrack
title: IMFTimedTextTrackList::GetTrack (mfmediaengine.h)
author: windows-sdk-content
description: Gets a text track in the list from the index of the track.
old-location: mf\imftimedtexttracklist_gettrack.htm
tech.root: medfound
ms.assetid: 5AF4F317-E46D-459A-900B-6D4796CD59A2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTrack, GetTrack method [Media Foundation], GetTrack method [Media Foundation],IMFTimedTextTrackList interface, IMFTimedTextTrackList interface [Media Foundation],GetTrack method, IMFTimedTextTrackList.GetTrack, IMFTimedTextTrackList::GetTrack, mf.imftimedtexttracklist_gettrack, mfmediaengine/IMFTimedTextTrackList::GetTrack
ms.topic: method
f1_keywords: ["mfmediaengine/IMFTimedTextTrackList.GetTrack"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextTrackList.GetTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextTrackList::GetTrack


## -description


Gets a text track in the list from the index of the track.


## -parameters




### -param index [in]

Type: <b>DWORD</b>

The index of the track in the list to retrieve.




### -param track [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a> interface for the timed-text track.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist">IMFTimedTextTrackList</a>
 

 

