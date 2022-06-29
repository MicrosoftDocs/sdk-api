---
UID: NF:winhttp.WinHttpUnregisterProxyChangeNotification
tech.root: http
title: WinHttpUnregisterProxyChangeNotification
ms.date: 06/29/2022
targetos: Windows
description: Unregisters a callback function that was registered by calling [WinHttpRegisterProxyChangeNotification](nf-winhttp-winhttpregisterproxychangenotification.md).
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
 - WinHttpUnregisterProxyChangeNotification
f1_keywords:
 - WinHttpUnregisterProxyChangeNotification
 - winhttp/WinHttpUnregisterProxyChangeNotification
dev_langs:
 - c++
helpviewer_keywords:
 - WinHttpUnregisterProxyChangeNotification
---

## -description

Unregisters a callback function that was registered by calling [WinHttpRegisterProxyChangeNotification](nf-winhttp-winhttpregisterproxychangenotification.md).

## -parameters

### -param hRegistration

Type: \_In\_ **WINHTTP_PROXY_CHANGE_REGISTRATION_HANDLE\***

The handle that was returned from [WinHttpRegisterProxyChangeNotification](nf-winhttp-winhttpregisterproxychangenotification.md).

## -returns

A **[DWORD](/windows/win32/winprog/windows-data-types)** containing a status code indicating the result of the operation.

## -remarks

## -see-also
