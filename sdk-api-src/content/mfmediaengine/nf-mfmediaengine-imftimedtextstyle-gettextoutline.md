---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetTextOutline
title: IMFTimedTextStyle::GetTextOutline (mfmediaengine.h)
author: windows-sdk-content
description: Gets the text outline for the timed-text style.
old-location: mf\imftimedtextstyle_gettextoutline.htm
tech.root: medfound
ms.assetid: 44701080-7E70-4073-85E2-4AF86D4B4FDB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTextOutline, GetTextOutline method [Media Foundation], GetTextOutline method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetTextOutline method, IMFTimedTextStyle.GetTextOutline, IMFTimedTextStyle::GetTextOutline, mf.imftimedtextstyle_gettextoutline, mfmediaengine/IMFTimedTextStyle::GetTextOutline
ms.topic: method
f1_keywords:
- mfmediaengine/IMFTimedTextStyle.GetTextOutline
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
- IMFTimedTextStyle.GetTextOutline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextStyle::GetTextOutline


## -description


Gets the text outline for the timed-text style.


## -parameters




### -param color [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that describes the color.


### -param thickness [out]

Type: <b>double*</b>

A pointer to a variable that receives the thickness.


### -param blurRadius [out]

Type: <b>double*</b>

A pointer to a variable that receives the blur radius.


### -param unitType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_unit_type">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>
 

 

