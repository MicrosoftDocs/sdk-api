---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetDisplayAlignment
title: IMFTimedTextRegion::GetDisplayAlignment (mfmediaengine.h)
description: Gets the display alignment of the region.
helpviewer_keywords: ["GetDisplayAlignment","GetDisplayAlignment method [Media Foundation]","GetDisplayAlignment method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetDisplayAlignment method","IMFTimedTextRegion.GetDisplayAlignment","IMFTimedTextRegion::GetDisplayAlignment","mf.imftimedtextregion_getdisplayalignment","mfmediaengine/IMFTimedTextRegion::GetDisplayAlignment"]
old-location: mf\imftimedtextregion_getdisplayalignment.htm
tech.root: mf
ms.assetid: CE2A9014-5510-4648-85F8-4A64C04C9F0C
ms.date: 12/05/2018
ms.keywords: GetDisplayAlignment, GetDisplayAlignment method [Media Foundation], GetDisplayAlignment method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetDisplayAlignment method, IMFTimedTextRegion.GetDisplayAlignment, IMFTimedTextRegion::GetDisplayAlignment, mf.imftimedtextregion_getdisplayalignment, mfmediaengine/IMFTimedTextRegion::GetDisplayAlignment
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
 - IMFTimedTextRegion::GetDisplayAlignment
 - mfmediaengine/IMFTimedTextRegion::GetDisplayAlignment
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
 - IMFTimedTextRegion.GetDisplayAlignment
---

# IMFTimedTextRegion::GetDisplayAlignment


## -description

Gets the display alignment of the region.

## -parameters

### -param displayAlign [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_display_alignment">MF_TIMED_TEXT_DISPLAY_ALIGNMENT</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_display_alignment">MF_TIMED_TEXT_DISPLAY_ALIGNMENT</a>-typed value that specifies the display alignment of the region.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>