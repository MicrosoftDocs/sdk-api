---
UID: NS:winhttp._WINHTTP_PROXY_SETTINGS_PARAM
tech.root: http
title: WINHTTP_PROXY_SETTINGS_PARAM
ms.date: 08/15/2022
targetos: Windows
description: The WINHTTP_PROXY_SETTINGS_PARAM structure represents extended proxy settings.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winhttp.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: WINHTTP_PROXY_SETTINGS_PARAM, *PWINHTTP_PROXY_SETTINGS_PARAM
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_PROXY_SETTINGS_PARAM
 - PWINHTTP_PROXY_SETTINGS_PARAM
 - WINHTTP_PROXY_SETTINGS_PARAM
f1_keywords:
 - _WINHTTP_PROXY_SETTINGS_PARAM
 - winhttp/_WINHTTP_PROXY_SETTINGS_PARAM
 - PWINHTTP_PROXY_SETTINGS_PARAM
 - winhttp/PWINHTTP_PROXY_SETTINGS_PARAM
 - WINHTTP_PROXY_SETTINGS_PARAM
 - winhttp/WINHTTP_PROXY_SETTINGS_PARAM
dev_langs:
 - c++
helpviewer_keywords:
 - _WINHTTP_PROXY_SETTINGS_PARAM
---

## -description

Represents extended proxy settings.

## -struct-fields

### -field ullFlags

Type: **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Flags.

### -field pcwszConnectionName

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The WCM connection name for which settings were retrieved.

### -field pcwszProbeHost

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

TBD

## -remarks

## -see-also
