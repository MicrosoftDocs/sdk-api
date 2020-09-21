---
UID: NF:mfmediaengine.IMFTimedTextNotify.Error
title: IMFTimedTextNotify::Error (mfmediaengine.h)
description: Called when an error occurs in a text track.
helpviewer_keywords: ["Error","Error method [Media Foundation]","Error method [Media Foundation]","IMFTimedTextNotify interface","IMFTimedTextNotify interface [Media Foundation]","Error method","IMFTimedTextNotify.Error","IMFTimedTextNotify::Error","mf.imftimedtextnotify_error","mfmediaengine/IMFTimedTextNotify::Error"]
old-location: mf\imftimedtextnotify_error.htm
tech.root: mf
ms.assetid: 3658EE26-497D-4D33-BE68-572BCE1B28B1
ms.date: 12/05/2018
ms.keywords: Error, Error method [Media Foundation], Error method [Media Foundation],IMFTimedTextNotify interface, IMFTimedTextNotify interface [Media Foundation],Error method, IMFTimedTextNotify.Error, IMFTimedTextNotify::Error, mf.imftimedtextnotify_error, mfmediaengine/IMFTimedTextNotify::Error
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
 - IMFTimedTextNotify::Error
 - mfmediaengine/IMFTimedTextNotify::Error
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
 - IMFTimedTextNotify.Error
---

# IMFTimedTextNotify::Error


## -description

Called when an error occurs in a text track.

## -parameters

### -param errorCode [in]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_error_code">MF_TIMED_TEXT_ERROR_CODE</a></b>

An MF_TIMED_TEXT_ERROR_CODE representing the last error.

### -param extendedErrorCode [in]

Type: <b>extendedErrorCode</b>

The extended error code for the last error.

### -param sourceTrackId [in]

Type: <b>extendedErrorCode</b>

The identifier of the track on which the error occurred.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify">IMFTimedTextNotify</a>