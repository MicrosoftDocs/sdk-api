---
UID: NF:mfmediaengine.IMFTimedTextTrackList.GetTrackById
title: IMFTimedTextTrackList::GetTrackById
author: windows-sdk-content
description: Gets a text track in the list from the identifier of the track.
old-location: mf\imftimedtexttracklist_gettrackbyid.htm
tech.root: medfound
ms.assetid: 5653ED8A-36B1-488C-9D76-50D64BA78BA8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetTrackById, GetTrackById method [Media Foundation], GetTrackById method [Media Foundation],IMFTimedTextTrackList interface, IMFTimedTextTrackList interface [Media Foundation],GetTrackById method, IMFTimedTextTrackList.GetTrackById, IMFTimedTextTrackList::GetTrackById, mf.imftimedtexttracklist_gettrackbyid, mfmediaengine/IMFTimedTextTrackList::GetTrackById
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFTimedTextTrackList.GetTrackById
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextTrackList::GetTrackById


## -description


Gets a text track in the list from the identifier of the track.


## -parameters




### -param trackId

TBD


### -param track

TBD




#### - dwTrackId [in]

Type: <b>DWORD</b>

The identifier of the track in the list to retrieve.




#### - ppTrack [out]

Type: <b><a href="https://msdn.microsoft.com/55232D19-F3D0-42C7-8B24-C2A7768B2C7E">IMFTimedTextTrack</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/55232D19-F3D0-42C7-8B24-C2A7768B2C7E">IMFTimedTextTrack</a> interface for the timed-text track.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EA94A81E-3B1D-4723-B00F-B216991E19E5">IMFTimedTextTrackList</a>
 

 

