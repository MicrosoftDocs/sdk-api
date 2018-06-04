---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



