---
UID: NF:mfmediaengine.IMFTimedText.GetTracks
title: IMFTimedText::GetTracks (mfmediaengine.h)
description: Retrieves a list of all timed-text tracks registered with the IMFTimedText.
helpviewer_keywords: ["GetTracks","GetTracks method [Media Foundation]","GetTracks method [Media Foundation]","IMFTimedText interface","IMFTimedText interface [Media Foundation]","GetTracks method","IMFTimedText.GetTracks","IMFTimedText::GetTracks","mf.imftimedtext_gettracks","mfmediaengine/IMFTimedText::GetTracks"]
old-location: mf\imftimedtext_gettracks.htm
tech.root: mf
ms.assetid: 4ECBC4CD-12A0-493A-A301-1E392F6EC280
ms.date: 12/05/2018
ms.keywords: GetTracks, GetTracks method [Media Foundation], GetTracks method [Media Foundation],IMFTimedText interface, IMFTimedText interface [Media Foundation],GetTracks method, IMFTimedText.GetTracks, IMFTimedText::GetTracks, mf.imftimedtext_gettracks, mfmediaengine/IMFTimedText::GetTracks
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
 - IMFTimedText::GetTracks
 - mfmediaengine/IMFTimedText::GetTracks
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
 - IMFTimedText.GetTracks
---

# IMFTimedText::GetTracks


## -description

Retrieves a list of all timed-text tracks registered with the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>.

## -parameters

### -param tracks [out]

Type: <b>IMFTimedTextTrackList**</b>

Receives a pointer to track list.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext">IMFTimedText</a>