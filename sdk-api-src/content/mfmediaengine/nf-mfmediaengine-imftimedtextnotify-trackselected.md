---
UID: NF:mfmediaengine.IMFTimedTextNotify.TrackSelected
title: IMFTimedTextNotify::TrackSelected (mfmediaengine.h)
description: Called when a track is selected or deselected.helpviewer_keywords: ["IMFTimedTextNotify interface [Media Foundation]","TrackSelected method","IMFTimedTextNotify.TrackSelected","IMFTimedTextNotify::TrackSelected","TrackSelected","TrackSelected method [Media Foundation]","TrackSelected method [Media Foundation]","IMFTimedTextNotify interface","mf.imftimedtextnotify_trackselected","mfmediaengine/IMFTimedTextNotify::TrackSelected"]
old-location: mf\imftimedtextnotify_trackselected.htm
tech.root: medfound
ms.assetid: C4757863-3D92-4D49-A2CA-8AD7C65461E6
ms.date: 12/05/2018
ms.keywords: IMFTimedTextNotify interface [Media Foundation],TrackSelected method, IMFTimedTextNotify.TrackSelected, IMFTimedTextNotify::TrackSelected, TrackSelected, TrackSelected method [Media Foundation], TrackSelected method [Media Foundation],IMFTimedTextNotify interface, mf.imftimedtextnotify_trackselected, mfmediaengine/IMFTimedTextNotify::TrackSelected
f1_keywords:
- mfmediaengine/IMFTimedTextNotify.TrackSelected
dev_langs:
- c++
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
- IMFTimedTextNotify.TrackSelected
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextNotify::TrackSelected


## -description


Called when a track is selected or deselected.


## -parameters




### -param trackId [in]

Type: <b>DWORD</b>

The identifier of the track that was selected or deselected.




### -param selected [in]

Type: <b>BOOL</b>

<b>TRUE</b> if the track was selected. <b>FALSE</b> if the track was deselected. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify">IMFTimedTextNotify</a>
 

 

