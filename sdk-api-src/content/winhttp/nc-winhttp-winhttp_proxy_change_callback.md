---
UID: NC:winhttp.WINHTTP_PROXY_CHANGE_CALLBACK
tech.root: http
title: WINHTTP_PROXY_CHANGE_CALLBACK
ms.date: 06/29/2022
targetos: Windows
description: Represents an application-defined proxy change callback function.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winhttp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - LibDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_PROXY_CHANGE_CALLBACK
f1_keywords:
 - WINHTTP_PROXY_CHANGE_CALLBACK
 - winhttp/WINHTTP_PROXY_CHANGE_CALLBACK
dev_langs:
 - c++
helpviewer_keywords:
 - WINHTTP_PROXY_CHANGE_CALLBACK
---

## -description

Represents an application-defined proxy change callback function.

## -parameters

### -param ullFlags

Type: \_In\_ **[ULONGLONG](/windows/win32/winprog/windows-data-types)**

The flag passed to the [WinHttpRegisterProxyChangeNotification](nf-winhttp-winhttpregisterproxychangenotification.md) function (for example, **WINHTTP_PROXY_NOTIFY_CHANGE**).

### -param pvContext

Type: \_In\_ **[PVOID](/windows/win32/winprog/windows-data-types)**

The context object pointer passed to the [WinHttpRegisterProxyChangeNotification](nf-winhttp-winhttpregisterproxychangenotification.md) function.

## -remarks

## -see-also
