---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetPosition
title: IMFTimedTextRegion::GetPosition (mfmediaengine.h)
description: Gets the position of the region.
helpviewer_keywords: ["GetPosition","GetPosition method [Media Foundation]","GetPosition method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetPosition method","IMFTimedTextRegion.GetPosition","IMFTimedTextRegion::GetPosition","mf.imftimedtextregion_getposition","mfmediaengine/IMFTimedTextRegion::GetPosition"]
old-location: mf\imftimedtextregion_getposition.htm
tech.root: mf
ms.assetid: 1DEE0689-A428-4121-9ED5-5E4D1376461E
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Media Foundation], GetPosition method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetPosition method, IMFTimedTextRegion.GetPosition, IMFTimedTextRegion::GetPosition, mf.imftimedtextregion_getposition, mfmediaengine/IMFTimedTextRegion::GetPosition
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
 - IMFTimedTextRegion::GetPosition
 - mfmediaengine/IMFTimedTextRegion::GetPosition
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
 - IMFTimedTextRegion.GetPosition
---

# IMFTimedTextRegion::GetPosition


## -description

Gets the position of the region.

## -parameters

### -param pX [out]

Type: <b>double*</b>

A pointer to a variable that receives the X-coordinate of the position.

### -param pY [out]

Type: <b>double*</b>

A pointer to a variable that receives the Y-coordinate of the position.

### -param unitType [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>