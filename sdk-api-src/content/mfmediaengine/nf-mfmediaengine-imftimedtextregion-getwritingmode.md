---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetWritingMode
title: IMFTimedTextRegion::GetWritingMode (mfmediaengine.h)
description: Gets the writing mode of the region.
helpviewer_keywords: ["GetWritingMode","GetWritingMode method [Media Foundation]","GetWritingMode method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetWritingMode method","IMFTimedTextRegion.GetWritingMode","IMFTimedTextRegion::GetWritingMode","mf.imftimedtextregion_getwritingmode","mfmediaengine/IMFTimedTextRegion::GetWritingMode"]
old-location: mf\imftimedtextregion_getwritingmode.htm
tech.root: mf
ms.assetid: BCF99D3C-554A-4788-B54B-236F463B1EAE
ms.date: 12/05/2018
ms.keywords: GetWritingMode, GetWritingMode method [Media Foundation], GetWritingMode method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetWritingMode method, IMFTimedTextRegion.GetWritingMode, IMFTimedTextRegion::GetWritingMode, mf.imftimedtextregion_getwritingmode, mfmediaengine/IMFTimedTextRegion::GetWritingMode
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
 - IMFTimedTextRegion::GetWritingMode
 - mfmediaengine/IMFTimedTextRegion::GetWritingMode
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
 - IMFTimedTextRegion.GetWritingMode
---

# IMFTimedTextRegion::GetWritingMode


## -description

Gets the writing mode of the region.

## -parameters

### -param writingMode [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_writing_mode">MF_TIMED_TEXT_WRITING_MODE</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_writing_mode">MF_TIMED_TEXT_WRITING_MODE</a>-typed value that specifies the writing mode of the region.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>