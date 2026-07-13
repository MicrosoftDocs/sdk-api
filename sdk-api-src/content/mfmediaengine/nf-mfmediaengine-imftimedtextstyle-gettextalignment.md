---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetTextAlignment
title: IMFTimedTextStyle::GetTextAlignment (mfmediaengine.h)
description: Gets the text alignment of the timed-text style.
helpviewer_keywords: ["GetTextAlignment","GetTextAlignment method [Media Foundation]","GetTextAlignment method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetTextAlignment method","IMFTimedTextStyle.GetTextAlignment","IMFTimedTextStyle::GetTextAlignment","mf.imftimedtextstyle_gettextalignment","mfmediaengine/IMFTimedTextStyle::GetTextAlignment"]
old-location: mf\imftimedtextstyle_gettextalignment.htm
tech.root: mf
ms.assetid: 2BB85E50-250C-4CFD-95DD-198899DCFE1D
ms.date: 12/05/2018
ms.keywords: GetTextAlignment, GetTextAlignment method [Media Foundation], GetTextAlignment method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetTextAlignment method, IMFTimedTextStyle.GetTextAlignment, IMFTimedTextStyle::GetTextAlignment, mf.imftimedtextstyle_gettextalignment, mfmediaengine/IMFTimedTextStyle::GetTextAlignment
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
 - IMFTimedTextStyle::GetTextAlignment
 - mfmediaengine/IMFTimedTextStyle::GetTextAlignment
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
 - IMFTimedTextStyle.GetTextAlignment
---

# IMFTimedTextStyle::GetTextAlignment


## -description

Gets the text alignment of the timed-text style.

## -parameters

### -param textAlign [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_alignment">MF_TIMED_TEXT_ALIGNMENT</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_alignment">MF_TIMED_TEXT_ALIGNMENT</a>-typed value that specifies the text alignment.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>