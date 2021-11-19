---
UID: NS:winhttp._WINHTTP_EXTENDED_HEADER
title: WINHTTP_EXTENDED_HEADER
description: Represents an HTTP request header as a name/value string pair.
tech.root: http
ms.date: 06/30/2021
req.construct-type: structure
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: WINHTTP_EXTENDED_HEADER, *PWINHTTP_EXTENDED_HEADER
req.redist: 
f1_keywords:
 - _WINHTTP_EXTENDED_HEADER
 - winhttp/_WINHTTP_EXTENDED_HEADER
 - PWINHTTP_EXTENDED_HEADER
 - winhttp/PWINHTTP_EXTENDED_HEADER
 - WINHTTP_EXTENDED_HEADER
 - winhttp/WINHTTP_EXTENDED_HEADER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_EXTENDED_HEADER
 - PWINHTTP_EXTENDED_HEADER
 - WINHTTP_EXTENDED_HEADER
---

## -description

Represents an HTTP request header as a name/value string pair.

## -struct-fields

### -field pwszName

Type: IN **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A wide string containing a name.

### -field pszName

Type: IN **[PCSTR](/windows/win32/winprog/windows-data-types)**

A narrow string containing a name.

### -field pwszValue

Type: IN **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A wide string containing a value.

### -field pszValue

Type: IN **[PCSTR](/windows/win32/winprog/windows-data-types)**

A narrow string containing a value.

## -remarks

## -see-also

* [WinHttpAddRequestHeadersEx](nf-winhttp-winhttpaddrequestheadersex.md)
