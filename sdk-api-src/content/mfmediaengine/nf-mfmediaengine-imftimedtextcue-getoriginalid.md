---
UID: NF:mfmediaengine.IMFTimedTextCue.GetOriginalId
title: IMFTimedTextCue::GetOriginalId (mfmediaengine.h)
description: Gets the cue identifier that is provided in the text-track data format, if available.
helpviewer_keywords: ["GetOriginalId","GetOriginalId method [Media Foundation]","GetOriginalId method [Media Foundation]","IMFTimedTextCue interface","IMFTimedTextCue interface [Media Foundation]","GetOriginalId method","IMFTimedTextCue.GetOriginalId","IMFTimedTextCue::GetOriginalId","mf.imftimedtextcue_getoriginalid","mfmediaengine/IMFTimedTextCue::GetOriginalId"]
old-location: mf\imftimedtextcue_getoriginalid.htm
tech.root: mf
ms.assetid: D5B94171-AEB0-4A7D-B596-F888B69A436D
ms.date: 12/05/2018
ms.keywords: GetOriginalId, GetOriginalId method [Media Foundation], GetOriginalId method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetOriginalId method, IMFTimedTextCue.GetOriginalId, IMFTimedTextCue::GetOriginalId, mf.imftimedtextcue_getoriginalid, mfmediaengine/IMFTimedTextCue::GetOriginalId
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
 - IMFTimedTextCue::GetOriginalId
 - mfmediaengine/IMFTimedTextCue::GetOriginalId
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
 - IMFTimedTextCue.GetOriginalId
---

# IMFTimedTextCue::GetOriginalId


## -description

Gets the cue identifier that is provided in the text-track data format, if available.

## -parameters

### -param originalId [out]

Type: <b>LPWSTR*</b>

The cue identifier that is provided in the text-track data format.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method retrieves an identifier for the cue that is included in the source data, if one was specified. The system dynamically generates identifiers for cues that are guaranteed to be unique within a single time-text track. To obtain this system-generated ID, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getid">GetId</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imftimedtextcue-getid">GetId</a>



<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>