---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetScrollMode
title: IMFTimedTextRegion::GetScrollMode (mfmediaengine.h)
description: Gets the scroll mode of the region.
helpviewer_keywords: ["GetScrollMode","GetScrollMode method [Media Foundation]","GetScrollMode method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetScrollMode method","IMFTimedTextRegion.GetScrollMode","IMFTimedTextRegion::GetScrollMode","mf.imftimedtextregion_getscrollmode","mfmediaengine/IMFTimedTextRegion::GetScrollMode"]
old-location: mf\imftimedtextregion_getscrollmode.htm
tech.root: mf
ms.assetid: 85CD2A7A-23ED-4D5C-AAEC-D5DF9F059897
ms.date: 12/05/2018
ms.keywords: GetScrollMode, GetScrollMode method [Media Foundation], GetScrollMode method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetScrollMode method, IMFTimedTextRegion.GetScrollMode, IMFTimedTextRegion::GetScrollMode, mf.imftimedtextregion_getscrollmode, mfmediaengine/IMFTimedTextRegion::GetScrollMode
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
 - IMFTimedTextRegion::GetScrollMode
 - mfmediaengine/IMFTimedTextRegion::GetScrollMode
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
 - IMFTimedTextRegion.GetScrollMode
---

# IMFTimedTextRegion::GetScrollMode


## -description

Gets the scroll mode of the region.

## -parameters

### -param scrollMode [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_scroll_mode">MF_TIMED_TEXT_SCROLL_MODE</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_scroll_mode">MF_TIMED_TEXT_SCROLL_MODE</a>-typed value that specifies the scroll mode of the region.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>