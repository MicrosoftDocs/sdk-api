---
UID: NF:mfmediaengine.IMFTimedTextCue.GetStyle
title: IMFTimedTextCue::GetStyle (mfmediaengine.h)
description: Gets info about the style of the timed-text cue.
helpviewer_keywords: ["GetStyle","GetStyle method [Media Foundation]","GetStyle method [Media Foundation]","IMFTimedTextCue interface","IMFTimedTextCue interface [Media Foundation]","GetStyle method","IMFTimedTextCue.GetStyle","IMFTimedTextCue::GetStyle","mf.imftimedtextcue_getstyle","mfmediaengine/IMFTimedTextCue::GetStyle"]
old-location: mf\imftimedtextcue_getstyle.htm
tech.root: mf
ms.assetid: 9E0B570D-69AA-449D-9988-96632A52756F
ms.date: 12/05/2018
ms.keywords: GetStyle, GetStyle method [Media Foundation], GetStyle method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetStyle method, IMFTimedTextCue.GetStyle, IMFTimedTextCue::GetStyle, mf.imftimedtextcue_getstyle, mfmediaengine/IMFTimedTextCue::GetStyle
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
 - IMFTimedTextCue::GetStyle
 - mfmediaengine/IMFTimedTextCue::GetStyle
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
 - IMFTimedTextCue.GetStyle
---

# IMFTimedTextCue::GetStyle


## -description

Gets info about the style  of the timed-text cue.

## -parameters

### -param style [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a> interface for the timed-text style. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>