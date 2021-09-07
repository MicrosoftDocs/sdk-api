---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetFontFamily
title: IMFTimedTextStyle::GetFontFamily (mfmediaengine.h)
description: Gets the font family of the timed-text style.
helpviewer_keywords: ["GetFontFamily","GetFontFamily method [Media Foundation]","GetFontFamily method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetFontFamily method","IMFTimedTextStyle.GetFontFamily","IMFTimedTextStyle::GetFontFamily","mf.imftimedtextstyle_getfontfamily","mfmediaengine/IMFTimedTextStyle::GetFontFamily"]
old-location: mf\imftimedtextstyle_getfontfamily.htm
tech.root: mf
ms.assetid: 4250F2ED-F479-45E9-89A3-9037F40BD4E2
ms.date: 12/05/2018
ms.keywords: GetFontFamily, GetFontFamily method [Media Foundation], GetFontFamily method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetFontFamily method, IMFTimedTextStyle.GetFontFamily, IMFTimedTextStyle::GetFontFamily, mf.imftimedtextstyle_getfontfamily, mfmediaengine/IMFTimedTextStyle::GetFontFamily
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
 - IMFTimedTextStyle::GetFontFamily
 - mfmediaengine/IMFTimedTextStyle::GetFontFamily
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
 - IMFTimedTextStyle.GetFontFamily
---

# IMFTimedTextStyle::GetFontFamily


## -description

Gets the font family of the timed-text style.

## -parameters

### -param fontFamily [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the font family of the style.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>