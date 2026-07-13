---
UID: NF:winnls.FILEMUIINFO_GET_CULTURE
title: FILEMUIINFO_GET_CULTURE macro (winnls.h)
description: Gets the locale name associated with the language name offset information in the dwLanguageNameOffset member of a FILEMUIINFO structure.
helpviewer_keywords: ["FILEMUIINFO_GET_CULTURE","FILEMUIINFO_GET_CULTURE macro [Internationalization for Windows Applications]","_win32_FILEMUIINFO_GET_CULTURE","intl.filemuiinfo_get_culture","winnls/FILEMUIINFO_GET_CULTURE"]
old-location: intl\filemuiinfo_get_culture.htm
tech.root: Intl
ms.assetid: 3afed0e8-3a9c-4513-954a-83855a53f5b2
ms.date: 07/01/2025
ms.keywords: FILEMUIINFO_GET_CULTURE, FILEMUIINFO_GET_CULTURE macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_CULTURE, intl.filemuiinfo_get_culture, winnls/FILEMUIINFO_GET_CULTURE
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - FILEMUIINFO_GET_CULTURE
 - winnls/FILEMUIINFO_GET_CULTURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - FILEMUIINFO_GET_CULTURE
---

# FILEMUIINFO_GET_CULTURE macro

## -syntax

```cpp
LPWSTR FILEMUIINFO_GET_CULTURE(
    PFILEMUIINFO pInfo
);
```

## -returns

Type: **LPWSTR**

Returns a pointer to the locale name. The macro returns **NULL** if the language name offset in the structure is not initialized.


## -description

Gets the locale name associated with the language name offset information in the <b>dwLanguageNameOffset</b> member of a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -parameters

### -param pInfo

Pointer to the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
