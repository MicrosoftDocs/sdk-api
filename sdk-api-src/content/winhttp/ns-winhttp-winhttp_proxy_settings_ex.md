---
UID: NS:winhttp._WINHTTP_PROXY_SETTINGS_EX
tech.root: http
title: WINHTTP_PROXY_SETTINGS_EX
ms.date: 08/15/2022
targetos: Windows
description: The WINHTTP_PROXY_SETTINGS_EX structure represents extended proxy settings.
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
req.typenames: WINHTTP_PROXY_SETTINGS_EX, *PWINHTTP_PROXY_SETTINGS_EX
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_PROXY_SETTINGS_EX
 - PWINHTTP_PROXY_SETTINGS_EX
 - WINHTTP_PROXY_SETTINGS_EX
f1_keywords:
 - _WINHTTP_PROXY_SETTINGS_EX
 - winhttp/_WINHTTP_PROXY_SETTINGS_EX
 - PWINHTTP_PROXY_SETTINGS_EX
 - winhttp/PWINHTTP_PROXY_SETTINGS_EX
 - WINHTTP_PROXY_SETTINGS_EX
 - winhttp/WINHTTP_PROXY_SETTINGS_EX
dev_langs:
 - c++
helpviewer_keywords:
 - _WINHTTP_PROXY_SETTINGS_EX
---

## -description

Represents extended proxy settings.

## -struct-fields

### -field ullGenerationId

Type: **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

The current network generation (incremented each time the configuration is changed).

### -field ullFlags

Type: **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

Flags for the proxy settings (for example, **WINHTTP_PROXY_TYPE_DIRECT**).

### -field pcwszAutoconfigUrl

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The PAC URL for the network (for example, L"http://proxy.contoso.com/wpad.dat").

### -field pcwszProxy

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The proxy address and port for HTTP traffic (for example, L"http://192.168.1.1:8888").

### -field pcwszSecureProxy

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The proxy address and port for HTTPS traffic (for example, L"http://192.168.1.1:8888").

### -field cProxyBypasses

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of entries in the proxy bypass list (*rgpcwszProxyBypasses*).

### -field rgpcwszProxyBypasses

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)\***

An array of strings containing each site in the proxy bypass list. (for example, L"contoso.com").

### -field dwInterfaceIndex

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The interface index for which settings were retrieved.

### -field pcwszConnectionName

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The WCM connection name for which settings were retrieved.

## -remarks

## -see-also
