---
UID: NF:mfmediaengine.IMFTimedTextCue.GetRegion
title: IMFTimedTextCue::GetRegion (mfmediaengine.h)
description: Gets info about the display region of the timed-text cue.
helpviewer_keywords: ["GetRegion","GetRegion method [Media Foundation]","GetRegion method [Media Foundation]","IMFTimedTextCue interface","IMFTimedTextCue interface [Media Foundation]","GetRegion method","IMFTimedTextCue.GetRegion","IMFTimedTextCue::GetRegion","mf.imftimedtextcue_getregion","mfmediaengine/IMFTimedTextCue::GetRegion"]
old-location: mf\imftimedtextcue_getregion.htm
tech.root: mf
ms.assetid: 8F5CE96E-9714-4F1A-8CB5-87FA24735B9D
ms.date: 12/05/2018
ms.keywords: GetRegion, GetRegion method [Media Foundation], GetRegion method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetRegion method, IMFTimedTextCue.GetRegion, IMFTimedTextCue::GetRegion, mf.imftimedtextcue_getregion, mfmediaengine/IMFTimedTextCue::GetRegion
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
 - IMFTimedTextCue::GetRegion
 - mfmediaengine/IMFTimedTextCue::GetRegion
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
 - IMFTimedTextCue.GetRegion
---

# IMFTimedTextCue::GetRegion


## -description

Gets info about the display region  of the timed-text cue.

## -parameters

### -param region [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a> interface for the timed-text region. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>