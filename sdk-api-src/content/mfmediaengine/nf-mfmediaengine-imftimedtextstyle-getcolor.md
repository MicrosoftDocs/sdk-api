---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetColor
title: IMFTimedTextStyle::GetColor (mfmediaengine.h)
description: Gets the color of the timed-text style.
helpviewer_keywords: ["GetColor","GetColor method [Media Foundation]","GetColor method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetColor method","IMFTimedTextStyle.GetColor","IMFTimedTextStyle::GetColor","mf.imftimedtextstyle_getcolor","mfmediaengine/IMFTimedTextStyle::GetColor"]
old-location: mf\imftimedtextstyle_getcolor.htm
tech.root: mf
ms.assetid: 262A89EC-7025-4037-B09A-87C9CEE1DF76
ms.date: 12/05/2018
ms.keywords: GetColor, GetColor method [Media Foundation], GetColor method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetColor method, IMFTimedTextStyle.GetColor, IMFTimedTextStyle::GetColor, mf.imftimedtextstyle_getcolor, mfmediaengine/IMFTimedTextStyle::GetColor
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
 - IMFTimedTextStyle::GetColor
 - mfmediaengine/IMFTimedTextStyle::GetColor
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
 - IMFTimedTextStyle.GetColor
---

# IMFTimedTextStyle::GetColor


## -description

Gets the color of the timed-text style.

## -parameters

### -param color [out]

Type: <b><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that describes the color.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>