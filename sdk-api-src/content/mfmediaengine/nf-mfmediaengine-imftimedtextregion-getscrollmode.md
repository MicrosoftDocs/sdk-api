---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetScrollMode
title: IMFTimedTextRegion::GetScrollMode (mfmediaengine.h)
description: Gets the scroll mode of the region.
old-location: mf\imftimedtextregion_getscrollmode.htm
tech.root: medfound
ms.assetid: 85CD2A7A-23ED-4D5C-AAEC-D5DF9F059897
ms.date: 12/05/2018
ms.keywords: GetScrollMode, GetScrollMode method [Media Foundation], GetScrollMode method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetScrollMode method, IMFTimedTextRegion.GetScrollMode, IMFTimedTextRegion::GetScrollMode, mf.imftimedtextregion_getscrollmode, mfmediaengine/IMFTimedTextRegion::GetScrollMode
f1_keywords:
- mfmediaengine/IMFTimedTextRegion.GetScrollMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFTimedTextRegion.GetScrollMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextRegion::GetScrollMode


## -description


Gets the scroll mode of the region.


## -parameters




### -param scrollMode [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_scroll_mode">MF_TIMED_TEXT_SCROLL_MODE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_scroll_mode">MF_TIMED_TEXT_SCROLL_MODE</a>-typed value that specifies the scroll mode of the region.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>
 

 

