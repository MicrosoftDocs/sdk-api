---
UID: NF:winhttp.WinHttpFreeProxySettingsEx
title: WinHttpFreeProxySettingsEx
description: Frees the data retrieved from a previous call to [WinHttpGetProxySettingsResultEx](nf-winhttp-winhttpgetproxysettingsresultex.md).
tech.root: http
ms.date: 06/29/2022
req.construct-type: function
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - WinHttpFreeProxySettingsEx
 - winhttp/WinHttpFreeProxySettingsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpFreeProxySettingsEx
helpviewer_keywords:
 - WinHttpFreeProxySettingsEx
---

## -description

Frees the data retrieved from a previous call to [WinHttpGetProxySettingsResultEx](nf-winhttp-winhttpgetproxysettingsresultex.md).

## -parameters

### -param ProxySettingsType

Type: \_In\_ **[WINHTTP_PROXY_SETTINGS_TYPE](/windows/win32/api/winhttp/ne-winhttp-winhttp_proxy_settings_type)**

A proxy settings type.

### -param pProxySettingsEx

Type: \_In\_ **[PVOID](/windows/win32/winprog/windows-data-types)**

A pointer to a [WINHTTP_PROXY_SETTINGS_EX](ns-winhttp-winhttp_proxy_settings_ex.md) structure that was retrieved from a previous call to [WinHttpGetProxySettingsResultEx](nf-winhttp-winhttpgetproxysettingsresultex.md).

## -returns

This function does not return a value.

## -remarks

## -see-also
