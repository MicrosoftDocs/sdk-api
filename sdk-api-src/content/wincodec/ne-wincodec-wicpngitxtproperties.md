---
UID: NE:wincodec.WICPngItxtProperties
title: WICPngItxtProperties
author: windows-sdk-content
description: Specifies the Portable Network Graphics (PNG) iTXT chunk metadata properties.
old-location: wic\_wic_codec_wicpngitxtproperties.htm
old-project: wic
ms.assetid: 905d37e2-39f3-4990-b737-f9194f798d83
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WICPngItxtCompressionFlag, WICPngItxtKeyword, WICPngItxtLanguageTag, WICPngItxtProperties, WICPngItxtProperties enumeration [Windows Imaging Component], WICPngItxtText, WICPngItxtTranslatedKeyword, _wic_codec_wicpngitxtproperties, wic._wic_codec_wicpngitxtproperties, wincodec/WICPngItxtCompressionFlag, wincodec/WICPngItxtKeyword, wincodec/WICPngItxtLanguageTag, wincodec/WICPngItxtProperties, wincodec/WICPngItxtText, wincodec/WICPngItxtTranslatedKeyword
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICPngItxtProperties
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICPngItxtProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICPngItxtProperties enumeration


## -description


Specifies the Portable Network Graphics (PNG) iTXT chunk metadata properties.


## -enum-fields




### -field WICPngItxtKeyword

[VT_LPSTR] Indicates the keywords in the iTXT metadata chunk.


### -field WICPngItxtCompressionFlag

[VT_UI1] Indicates whether the text in the iTXT chunk is compressed. 1 if the text is compressed; otherwise, 0.


### -field WICPngItxtLanguageTag

[VT_LPSTR] Indicates the human language used by the translated keyword and the text.


### -field WICPngItxtTranslatedKeyword

[VT_LPWSTR] Indicates a translation of the keyword into the language indicated by the language tag.


### -field WICPngItxtText

[VT_LPWSTR] Indicates additional text in the iTXT metadata chunk.


### -field WICPngItxtProperties_FORCE_DWORD



