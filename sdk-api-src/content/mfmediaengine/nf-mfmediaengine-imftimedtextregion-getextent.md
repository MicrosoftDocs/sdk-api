---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetExtent
title: IMFTimedTextRegion::GetExtent (mfmediaengine.h)
description: Gets the extent of the region.
old-location: mf\imftimedtextregion_getextent.htm
tech.root: medfound
ms.assetid: 581D9A8D-FBED-4E67-9E81-77D9C29ADF82
ms.date: 12/05/2018
ms.keywords: GetExtent, GetExtent method [Media Foundation], GetExtent method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetExtent method, IMFTimedTextRegion.GetExtent, IMFTimedTextRegion::GetExtent, mf.imftimedtextregion_getextent, mfmediaengine/IMFTimedTextRegion::GetExtent
f1_keywords:
- mfmediaengine/IMFTimedTextRegion.GetExtent
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
- IMFTimedTextRegion.GetExtent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextRegion::GetExtent


## -description


Gets the extent of the region.


## -parameters




### -param pWidth [out]

Type: <b>double*</b>

A pointer to a variable that receives the width of the region.


### -param pHeight [out]

Type: <b>double*</b>

A pointer to a variable that receives the height of the region.


### -param unitType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>
 

 

