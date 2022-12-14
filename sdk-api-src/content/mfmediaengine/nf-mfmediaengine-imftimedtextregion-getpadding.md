---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetPadding
title: IMFTimedTextRegion::GetPadding (mfmediaengine.h)
description: Gets the padding that surrounds the region.
helpviewer_keywords: ["GetPadding","GetPadding method [Media Foundation]","GetPadding method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetPadding method","IMFTimedTextRegion.GetPadding","IMFTimedTextRegion::GetPadding","mf.imftimedtextregion_getpadding","mfmediaengine/IMFTimedTextRegion::GetPadding"]
old-location: mf\imftimedtextregion_getpadding.htm
tech.root: mf
ms.assetid: B97ECFD8-2E96-425F-B29E-49E7D53BBFCB
ms.date: 12/05/2018
ms.keywords: GetPadding, GetPadding method [Media Foundation], GetPadding method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetPadding method, IMFTimedTextRegion.GetPadding, IMFTimedTextRegion::GetPadding, mf.imftimedtextregion_getpadding, mfmediaengine/IMFTimedTextRegion::GetPadding
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
 - IMFTimedTextRegion::GetPadding
 - mfmediaengine/IMFTimedTextRegion::GetPadding
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
 - IMFTimedTextRegion.GetPadding
---

# IMFTimedTextRegion::GetPadding


## -description

Gets the padding that surrounds the region.

## -parameters

### -param before [out]

Type: <b>double*</b>

A pointer to a variable that receives the padding before the start of the region.

### -param start [out]

Type: <b>double*</b>

A pointer to a variable that receives the start of the region.

### -param after [out]

Type: <b>double*</b>

A pointer to a variable that receives the padding after the end of the region.

### -param end [out]

Type: <b>double*</b>

A pointer to a variable that receives the end of the region.

### -param unitType [out]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>