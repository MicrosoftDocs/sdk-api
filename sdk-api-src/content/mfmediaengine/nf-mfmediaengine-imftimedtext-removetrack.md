---
UID: NF:mfmediaengine.IMFTimedText.RemoveTrack
title: IMFTimedText::RemoveTrack (mfmediaengine.h)
description: Removes the timed-text track with the specified identifier.
helpviewer_keywords: ["IMFTimedText interface [Media Foundation]","RemoveTrack method","IMFTimedText.RemoveTrack","IMFTimedText::RemoveTrack","RemoveTrack","RemoveTrack method [Media Foundation]","RemoveTrack method [Media Foundation]","IMFTimedText interface","mf.imftimedtext_removetrack","mfmediaengine/IMFTimedText::RemoveTrack"]
old-location: mf\imftimedtext_removetrack.htm
tech.root: mf
ms.assetid: 34B785F6-0B34-431A-91CD-3C2DCEFEDAA4
ms.date: 12/05/2018
ms.keywords: IMFTimedText interface [Media Foundation],RemoveTrack method, IMFTimedText.RemoveTrack, IMFTimedText::RemoveTrack, RemoveTrack, RemoveTrack method [Media Foundation], RemoveTrack method [Media Foundation],IMFTimedText interface, mf.imftimedtext_removetrack, mfmediaengine/IMFTimedText::RemoveTrack
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimedText::RemoveTrack
 - mfmediaengine/IMFTimedText::RemoveTrack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.dll
api_name:
 - IMFTimedText.RemoveTrack
---

# IMFTimedText::RemoveTrack


## -description

Removes the timed-text track with the specified identifier.

## -parameters

### -param track [in]

Type: <b>DWORD</b>

The identifier of the track to remove.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Get the identifier for a track by calling <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtexttrack-getid">GetId</a>. 

When a track is removed, all buffered data from the track is also removed.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>