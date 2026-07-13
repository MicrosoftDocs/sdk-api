---
UID: NF:mfmediaengine.IMFTimedText.SelectTrack
title: IMFTimedText::SelectTrack (mfmediaengine.h)
description: Selects or deselects a track of text in the timed-text component.
helpviewer_keywords: ["IMFTimedText interface [Media Foundation]","SelectTrack method","IMFTimedText.SelectTrack","IMFTimedText::SelectTrack","SelectTrack","SelectTrack method [Media Foundation]","SelectTrack method [Media Foundation]","IMFTimedText interface","mf.imftimedtext_selecttrack","mfmediaengine/IMFTimedText::SelectTrack"]
old-location: mf\imftimedtext_selecttrack.htm
tech.root: mf
ms.assetid: 868FE620-6FF3-4623-BB61-B47D0290D005
ms.date: 12/05/2018
ms.keywords: IMFTimedText interface [Media Foundation],SelectTrack method, IMFTimedText.SelectTrack, IMFTimedText::SelectTrack, SelectTrack, SelectTrack method [Media Foundation], SelectTrack method [Media Foundation],IMFTimedText interface, mf.imftimedtext_selecttrack, mfmediaengine/IMFTimedText::SelectTrack
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
 - IMFTimedText::SelectTrack
 - mfmediaengine/IMFTimedText::SelectTrack
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
 - IMFTimedText.SelectTrack
---

# IMFTimedText::SelectTrack


## -description

Selects or deselects a track of text in the timed-text component.

## -parameters

### -param trackId [in]

Type: <b>DWORD</b>

The identifier of the track to select.

### -param selected [in]

Type: <b>BOOL</b>

Specifies whether to select or deselect a track of text. Specify <b>TRUE</b> to select the track or <b>FALSE</b> to deselect the track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>