---
UID: NF:mfmediaengine.IMFTimedTextTrack.GetLabel
title: IMFTimedTextTrack::GetLabel (mfmediaengine.h)
description: Gets the label of the track.
helpviewer_keywords: ["GetLabel","GetLabel method [Media Foundation]","GetLabel method [Media Foundation]","IMFTimedTextTrack interface","IMFTimedTextTrack interface [Media Foundation]","GetLabel method","IMFTimedTextTrack.GetLabel","IMFTimedTextTrack::GetLabel","mf.imftimedtexttrack_getlabel","mfmediaengine/IMFTimedTextTrack::GetLabel"]
old-location: mf\imftimedtexttrack_getlabel.htm
tech.root: mf
ms.assetid: BB3B1089-6489-4C70-BAFD-22D72DE3CB38
ms.date: 12/05/2018
ms.keywords: GetLabel, GetLabel method [Media Foundation], GetLabel method [Media Foundation],IMFTimedTextTrack interface, IMFTimedTextTrack interface [Media Foundation],GetLabel method, IMFTimedTextTrack.GetLabel, IMFTimedTextTrack::GetLabel, mf.imftimedtexttrack_getlabel, mfmediaengine/IMFTimedTextTrack::GetLabel
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
 - IMFTimedTextTrack::GetLabel
 - mfmediaengine/IMFTimedTextTrack::GetLabel
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
 - IMFTimedTextTrack.GetLabel
---

# IMFTimedTextTrack::GetLabel


## -description

Gets the label of the track.

## -parameters

### -param label [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the label of the track.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack">IMFTimedTextTrack</a>