---
UID: NF:winhttp.WinHttpRegisterProxyChangeNotification
tech.root: http
title: WinHttpRegisterProxyChangeNotification
ms.date: 06/29/2022
targetos: Windows
description: Registers a callback function that WinHTTP calls when the effective proxy settings change.
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
 - WinHttpRegisterProxyChangeNotification
f1_keywords:
 - WinHttpRegisterProxyChangeNotification
 - winhttp/WinHttpRegisterProxyChangeNotification
dev_langs:
 - c++
helpviewer_keywords:
 - WinHttpRegisterProxyChangeNotification
---

## -description

Registers a callback function that WinHTTP calls when the effective proxy settings change.

## -parameters

### -param ullFlags

Type: \_In\_ **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

The flag to pass to the callback (for example, **WINHTTP_PROXY_NOTIFY_CHANGE**).

### -param pfnCallback

Type: \_In\_ **[WINHTTP_PROXY_CHANGE_CALLBACK](nc-winhttp-winhttp_proxy_change_callback.md)**

A pointer to the callback function that should be called when the effective proxy settings change.

### -param pvContext

Type: \_In\_ **[PVOID](/windows/win32/winprog/windows-data-types)**

A pointer to a context object to pass to the callback.

### -param hRegistration

Type: \_Out\_ **WINHTTP_PROXY_CHANGE_REGISTRATION_HANDLE\***

A handle that identifies the registration of the callback function. To unregister, pass this value to [WinHttpUnregisterProxyChangeNotification](nf-winhttp-winhttpunregisterproxychangenotification.md). **WINHTTP_PROXY_CHANGE_REGISTRATION_HANDLE** is equivalent to [PVOID](/windows/win32/winprog/windows-data-types).

## -returns

A **[DWORD](/windows/win32/winprog/windows-data-types)** containing a status code indicating the result of the operation. The following codes can be returned (the list is not exhaustive).

|Code|Description|
|-|-|
|ERROR_SUCCESS|The operation succeeded.|

## -remarks

## -see-also
