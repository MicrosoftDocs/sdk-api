---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetBold
title: IMFTimedTextStyle::GetBold (mfmediaengine.h)
description: Determines whether the style of timed text is bold.
helpviewer_keywords: ["GetBold","GetBold method [Media Foundation]","GetBold method [Media Foundation]","IMFTimedTextStyle interface","IMFTimedTextStyle interface [Media Foundation]","GetBold method","IMFTimedTextStyle.GetBold","IMFTimedTextStyle::GetBold","mf.imftimedtextstyle_getbold","mfmediaengine/IMFTimedTextStyle::GetBold"]
old-location: mf\imftimedtextstyle_getbold.htm
tech.root: mf
ms.assetid: 53CAE4C9-061B-44F3-A81B-A276085C69F2
ms.date: 12/05/2018
ms.keywords: GetBold, GetBold method [Media Foundation], GetBold method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetBold method, IMFTimedTextStyle.GetBold, IMFTimedTextStyle::GetBold, mf.imftimedtextstyle_getbold, mfmediaengine/IMFTimedTextStyle::GetBold
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
 - IMFTimedTextStyle::GetBold
 - mfmediaengine/IMFTimedTextStyle::GetBold
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
 - IMFTimedTextStyle.GetBold
---

# IMFTimedTextStyle::GetBold


## -description

Determines whether the style  of timed text is bold.

## -parameters

### -param bold [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether the style  of timed text is bold. The variable specifies <b>TRUE</b> if the style is bold; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>