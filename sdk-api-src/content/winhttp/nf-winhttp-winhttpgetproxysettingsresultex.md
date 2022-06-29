---
UID: NF:winhttp.WinHttpGetProxySettingsResultEx
tech.root: http
title: WinHttpGetProxySettingsResultEx
ms.date: 06/29/2022
targetos: Windows
description: Retrieves the results of a call to [WinHttpGetProxySettingsEx](nf-winhttp-winhttpgetproxysettingsex.md).
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
 - WinHttpGetProxySettingsResultEx
f1_keywords:
 - WinHttpGetProxySettingsResultEx
 - winhttp/WinHttpGetProxySettingsResultEx
dev_langs:
 - c++
helpviewer_keywords:
 - WinHttpGetProxySettingsResultEx
---

## -description

Retrieves the results of a call to [WinHttpGetProxySettingsEx](nf-winhttp-winhttpgetproxysettingsex.md).

## -parameters

### -param hResolver

Type: \_In\_ **[HINTERNET](/windows/win32/winprog/windows-data-types)**

The resolver handle used to issue a previously completed call to [WinHttpGetProxySettingsEx](nf-winhttp-winhttpgetproxysettingsex.md).

### -param pProxySettingsEx

A pointer to a [WINHTTP_PROXY_SETTINGS_EX](ns-winhttp-winhttp_proxy_settings_ex.md) structure. The memory occupied by the structure is allocated by **WinHttpGetProxySettingsResultEx**, so you need to free that memory by passing this pointer to [WinHttpFreeProxySettingsEx](nf-winhttp-winhttpfreeproxysettingsex.md).

## -returns

## -remarks

## -see-also
