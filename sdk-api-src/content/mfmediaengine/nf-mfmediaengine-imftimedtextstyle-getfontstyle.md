---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetFontStyle
title: IMFTimedTextStyle::GetFontStyle (mfmediaengine.h)
author: windows-sdk-content
description: Gets the font style of the timed-text style.
old-location: mf\imftimedtextstyle_getfontstyle.htm
tech.root: medfound
ms.assetid: 4089F237-BDA6-49AF-967F-089D641D4B09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFontStyle, GetFontStyle method [Media Foundation], GetFontStyle method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetFontStyle method, IMFTimedTextStyle.GetFontStyle, IMFTimedTextStyle::GetFontStyle, mf.imftimedtextstyle_getfontstyle, mfmediaengine/IMFTimedTextStyle::GetFontStyle
ms.topic: method
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
 - IMFTimedTextStyle.GetFontStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextStyle::GetFontStyle


## -description


Gets the font style of the timed-text style.


## -parameters




### -param fontStyle [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_font_style">MF_TIMED_TEXT_FONT_STYLE</a>*</b>

A pointer to a variable that receives a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_font_style">MF_TIMED_TEXT_FONT_STYLE</a>-typed value that specifies the font style.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle">IMFTimedTextStyle</a>
 

 

