---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetFontFamily
title: IMFTimedTextStyle::GetFontFamily
author: windows-sdk-content
description: Gets the font family of the timed-text style.
old-location: mf\imftimedtextstyle_getfontfamily.htm
old-project: medfound
ms.assetid: 4250F2ED-F479-45E9-89A3-9037F40BD4E2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetFontFamily, GetFontFamily method [Media Foundation], GetFontFamily method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetFontFamily method, IMFTimedTextStyle.GetFontFamily, IMFTimedTextStyle::GetFontFamily, mf.imftimedtextstyle_getfontfamily, mfmediaengine/IMFTimedTextStyle::GetFontFamily
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextStyle.GetFontFamily
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextStyle::GetFontFamily


## -description


Gets the font family of the timed-text style.


## -parameters




### -param fontFamily






#### - ppFontFamily [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the font family of the style.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

