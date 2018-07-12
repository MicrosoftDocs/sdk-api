---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetFontStyle
title: IMFTimedTextStyle::GetFontStyle
author: windows-sdk-content
description: Gets the font style of the timed-text style.
old-location: mf\imftimedtextstyle_getfontstyle.htm
old-project: medfound
ms.assetid: 4089F237-BDA6-49AF-967F-089D641D4B09
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetFontStyle, GetFontStyle method [Media Foundation], GetFontStyle method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetFontStyle method, IMFTimedTextStyle.GetFontStyle, IMFTimedTextStyle::GetFontStyle, mf.imftimedtextstyle_getfontstyle, mfmediaengine/IMFTimedTextStyle::GetFontStyle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextStyle::GetFontStyle


## -description


Gets the font style of the timed-text style.


## -parameters




### -param fontStyle






#### - pFontStyle [out]

Type: <b><a href="https://msdn.microsoft.com/29D8CCBD-B69A-46B5-8320-06C0E2EA81AE">MF_TIMED_TEXT_FONT_STYLE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/29D8CCBD-B69A-46B5-8320-06C0E2EA81AE">MF_TIMED_TEXT_FONT_STYLE</a>-typed value that specifies the font style.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

