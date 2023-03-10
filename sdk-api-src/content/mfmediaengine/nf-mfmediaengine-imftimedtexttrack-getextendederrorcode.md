---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetExtendedErrorCode
title: IMFTimedTextTrack::GetExtendedErrorCode (mfmediaengine.h)
description: Gets the extended error code for the latest error associated with the track.
helpviewer_keywords: ["GetExtendedErrorCode","GetExtendedErrorCode method [Media Foundation]","GetExtendedErrorCode method [Media Foundation]","IMFTimedTextTrack interface","IMFTimedTextTrack interface [Media Foundation]","GetExtendedErrorCode method","IMFTimedTextTrack.GetExtendedErrorCode","IMFTimedTextTrack::GetExtendedErrorCode","mf.imftimedtexttrack_getextendederrorcode","mfmediaengine/IMFTimedTextTrack::GetExtendedErrorCode"]
old-location: mf\imftimedtexttrack_getextendederrorcode.htm
tech.root: mf
ms.assetid: 61119103-B6F6-414B-AA7E-55DC889A5C28
ms.date: 12/05/2018
ms.keywords: GetExtendedErrorCode, GetExtendedErrorCode method [Media Foundation], GetExtendedErrorCode method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetExtendedErrorCode method, IMFTimedTextTrack.GetExtendedErrorCode, IMFTimedTextTrack::GetExtendedErrorCode, mf.imftimedtexttrack_getextendederrorcode, mfmediaengine/IMFTimedTextTrack::GetExtendedErrorCode
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
 - IMFTimedTextTrack::GetExtendedErrorCode
 - mfmediaengine/IMFTimedTextTrack::GetExtendedErrorCode
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
 - IMFTimedTextTrack.GetExtendedErrorCode
---

# IMFTimedTextTrack::GetExtendedErrorCode


## -description

Gets the extended error code for the latest error associated with the track.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The extended error code for the latest error associated with the track.

## -remarks

If the most recent error was associated with a track, this value will be the same <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> as returned by the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextnotify-error">IMFTimedTextNotify::Error</a> method.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>
