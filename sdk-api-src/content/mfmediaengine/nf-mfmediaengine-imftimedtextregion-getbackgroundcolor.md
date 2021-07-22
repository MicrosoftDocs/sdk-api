---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetBackgroundColor
title: IMFTimedTextRegion::GetBackgroundColor (mfmediaengine.h)
description: Gets the background color of the region.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [Media Foundation]","GetBackgroundColor method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetBackgroundColor method","IMFTimedTextRegion.GetBackgroundColor","IMFTimedTextRegion::GetBackgroundColor","mf.imftimedtextregion_getbackgroundcolor","mfmediaengine/IMFTimedTextRegion::GetBackgroundColor"]
old-location: mf\imftimedtextregion_getbackgroundcolor.htm
tech.root: mf
ms.assetid: E92FFB7E-C364-43C8-82CF-C3B4116C4187
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Media Foundation], GetBackgroundColor method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetBackgroundColor method, IMFTimedTextRegion.GetBackgroundColor, IMFTimedTextRegion::GetBackgroundColor, mf.imftimedtextregion_getbackgroundcolor, mfmediaengine/IMFTimedTextRegion::GetBackgroundColor
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
 - IMFTimedTextRegion::GetBackgroundColor
 - mfmediaengine/IMFTimedTextRegion::GetBackgroundColor
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
 - IMFTimedTextRegion.GetBackgroundColor
---

# IMFTimedTextRegion::GetBackgroundColor


## -description

Gets the background color of the region.

## -parameters

### -param bgColor [out]

Type: <b><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that describes the background color.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>