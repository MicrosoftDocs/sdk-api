---
UID: NF:mfmediaengine.IMFTimedTextTrack.SetLabel
title: IMFTimedTextTrack::SetLabel (mfmediaengine.h)
description: Sets the label of a timed-text track.
helpviewer_keywords: ["IMFTimedTextTrack interface [Media Foundation]","SetLabel method","IMFTimedTextTrack.SetLabel","IMFTimedTextTrack::SetLabel","SetLabel","SetLabel method [Media Foundation]","SetLabel method [Media Foundation]","IMFTimedTextTrack interface","mf.imftimedtexttrack_setlabel","mfmediaengine/IMFTimedTextTrack::SetLabel"]
old-location: mf\imftimedtexttrack_setlabel.htm
tech.root: mf
ms.assetid: 751CBF14-C445-4F2A-96F6-CB6159FAA1EE
ms.date: 12/05/2018
ms.keywords: IMFTimedTextTrack interface [Media Foundation],SetLabel method, IMFTimedTextTrack.SetLabel, IMFTimedTextTrack::SetLabel, SetLabel, SetLabel method [Media Foundation], SetLabel method [Media Foundation],IMFTimedTextTrack interface, mf.imftimedtexttrack_setlabel, mfmediaengine/IMFTimedTextTrack::SetLabel
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
 - IMFTimedTextTrack::SetLabel
 - mfmediaengine/IMFTimedTextTrack::SetLabel
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
 - IMFTimedTextTrack.SetLabel
---

# IMFTimedTextTrack::SetLabel


## -description

Sets the label of a timed-text track.

## -parameters

### -param label [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated wide-character string that contains the label of the track.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>