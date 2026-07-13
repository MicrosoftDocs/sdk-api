---
UID: NF:bcp47mrm.IsWellFormedTag
tech.root: menurc
title: IsWellFormedTag
ms.date: 05/12/2021
targetos: Windows
description: Determines whether a BCP-47 language tag is well-formed.
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
 - IsWellFormedTag
f1_keywords:
 - IsWellFormedTag
 - bcp47mrm/IsWellFormedTag
dev_langs:
 - c++
---

## -description

Determines whether a [BCP-47](https://tools.ietf.org/html/bcp47) language tag is well-formed.

## -parameters

### -param pszTag

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A [BCP-47](https://tools.ietf.org/html/bcp47) language tag.

## -returns

`true` if the language tag is well-formed as defined by [BCP-47](https://tools.ietf.org/html/bcp47), except when the language tag can never be valid according to BCP-47. Otherwise it returns `false`.

## -remarks

If this function returns `true`, an application can safely construct a Windows Runtime [Language](https://docs.microsoft.com/uwp/api/Windows.Globalization.Language) by using this tag. If it returns `false`, attempting to construct a Language for the given tag will throw an exception.

## -see-also

[BCP-47 language tags](https://tools.ietf.org/html/bcp47)
