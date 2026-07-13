---
UID: NF:winhttp.WinHttpGetProxySettingsEx
tech.root: http
title: WinHttpGetProxySettingsEx
ms.date: 06/29/2022
targetos: Windows
description: Retrieves extended proxy settings.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.header: winhttp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpGetProxySettingsEx
f1_keywords:
 - WinHttpGetProxySettingsEx
 - winhttp/WinHttpGetProxySettingsEx
dev_langs:
 - c++
helpviewer_keywords:
 - WinHttpGetProxySettingsEx
---

## -description

Retrieves extended proxy settings.

## -parameters

### -param hResolver

Type: \_In\_ **[HINTERNET](/windows/win32/winprog/windows-data-types)**

The WinHTTP resolver handle returned by the [WinHttpCreateProxyResolver](nf-winhttp-winhttpcreateproxyresolver.md) function.

### -param ProxySettingsType

Type: \_In\_ **[WINHTTP_PROXY_SETTINGS_TYPE](/windows/win32/api/winhttp/ne-winhttp-winhttp_proxy_settings_type)**

A proxy settings type.

### -param pProxySettingsParam

Type: \_In\_opt\_ **[PWINHTTP_PROXY_SETTINGS_PARAM](ns-winhttp-winhttp_proxy_settings_param.md)**

An optional pointer to a [WINHTTP_PROXY_SETTINGS_PARAM](ns-winhttp-winhttp_proxy_settings_param.md).

### -param pContext

Type: \_In\_opt\_ **[DWORD_PTR](/windows/win32/winprog/windows-data-types)**

An optional pointer to a **[DWORD](/windows/win32/winprog/windows-data-types)** containing context data that will be passed to the completion callback function.

## -returns

A **[DWORD](/windows/win32/winprog/windows-data-types)** containing a status code indicating the result of the operation. The following codes can be returned (the list is not exhaustive).

|Code|Description|
|-|-|
|ERROR_IO_PENDING|The operation is continuing asynchronously.|

## -remarks

## -see-also
