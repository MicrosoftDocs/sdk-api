---
UID: NF:bcp47mrm.GetDistanceOfClosestLanguageInList
tech.root: menurc
title: GetDistanceOfClosestLanguageInList
ms.date: 05/12/2021
targetos: Windows
description: Determines the distance between the specified language code and the closest match in a list of languages.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: bcp47mrm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: bcp47mrm.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 17763 
req.target-min-winversvr: Windows 10 Build 17763
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bcp47mrm.h
api_name:
 - GetDistanceOfClosestLanguageInList
f1_keywords:
 - GetDistanceOfClosestLanguageInList
 - bcp47mrm/GetDistanceOfClosestLanguageInList
dev_langs:
 - c++
---

## -description

Determines the distance between the specified language tag and the closest match in a list of languages.

## -parameters

### -param pszLanguage

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A [BCP-47](https://tools.ietf.org/html/bcp47) language tag that represents the candidate language.

### -param pszLanguagesList

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A character delimited list of [BCP-47](https://tools.ietf.org/html/bcp47) language tags to compare to the candidate language. This is typically the list of user languages.

If the *wchListDelimiter* parameter is `L'\0'`, then the *pszLanguagesList* is a double null-terminated list of language tags.
Otherwise, the *pszLanguagesList* is a null-terminated string in which the language tags are separated by the provided delimiter.

### -param wchListDelimiter

Type: **[wchar_t](/windows/win32/midl/wchar-t)**

The character used as a delimiter in the language list, or `L'\0'` to indicate that the language list is a double null-terminated list.
The function is slightly more efficient if this parameter is `L'\0'`.

### -param pClosestDistance

Type: **[double](/windows/win32/midl/double)**

Receives the distance between the candidate language and the closest language in the list.
The value is in the range 0.0 to 1.0, where 1.0 is an exact match.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If there is no match to any language in the list, the function returns `HRESULT_FROM_WIN32(ERROR_NO_MATCH)`
and a distance of 0.0.

## -remarks

You can use this function for localization to find the closest match to a candidate language in the list of user languages.

## -see-also

[IsWellFormedTag](nf-bcp47mrm-iswellformedtag.md), [BCP-47 language tags](https://tools.ietf.org/html/bcp47)
