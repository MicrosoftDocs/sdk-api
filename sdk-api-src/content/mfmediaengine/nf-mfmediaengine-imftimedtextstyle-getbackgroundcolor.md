---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetBackgroundColor
title: IMFTimedTextStyle::GetBackgroundColor (mfmediaengine.h)
description: Gets the background color of the timed-text style.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [Media Foundation]","GetBackgroundColor method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetBackgroundColor method","IMFTimedTextStyle.GetBackgroundColor","IMFTimedTextStyle::GetBackgroundColor","mf.imftimedtextstyle_getbackgroundcolor","mfmediaengine/IMFTimedTextStyle::GetBackgroundColor"]
old-location: mf\imftimedtextstyle_getbackgroundcolor.htm
tech.root: mf
ms.assetid: 2641F157-31CE-4659-AF6B-B57774AEF4E5
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Media Foundation], GetBackgroundColor method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetBackgroundColor method, IMFTimedTextStyle.GetBackgroundColor, IMFTimedTextStyle::GetBackgroundColor, mf.imftimedtextstyle_getbackgroundcolor, mfmediaengine/IMFTimedTextStyle::GetBackgroundColor
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
 - IMFTimedTextStyle::GetBackgroundColor
 - mfmediaengine/IMFTimedTextStyle::GetBackgroundColor
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
 - IMFTimedTextStyle.GetBackgroundColor
---

# IMFTimedTextStyle::GetBackgroundColor


## -description

Gets the background color of the timed-text style.

## -parameters

### -param bgColor [out]

Type: <b><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that describes the background color.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>