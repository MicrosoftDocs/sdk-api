---
UID: NS:winhttp._WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
title: WINHTTP_CURRENT_USER_IE_PROXY_CONFIG (winhttp.h)
description: The WINHTTP_CURRENT_USER_IE_PROXY_CONFIG structure contains the Internet Explorer proxy configuration information.
helpviewer_keywords: ["WINHTTP_CURRENT_USER_IE_PROXY_CONFIG","WINHTTP_CURRENT_USER_IE_PROXY_CONFIG structure [HTTP]","http.winhttp_current_user_ie_proxy_config","winhttp/WINHTTP_CURRENT_USER_IE_PROXY_CONFIG"]
old-location: http\winhttp_current_user_ie_proxy_config.htm
tech.root: http
ms.assetid: b5aebbfe-18c8-4aeb-a01b-488e37d227a1
ms.date: 12/05/2018
ms.keywords: WINHTTP_CURRENT_USER_IE_PROXY_CONFIG, WINHTTP_CURRENT_USER_IE_PROXY_CONFIG structure [HTTP], http.winhttp_current_user_ie_proxy_config, winhttp/WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
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
req.typenames: WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
 - winhttp/WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_CURRENT_USER_IE_PROXY_CONFIG
---

## -description

The <b>WINHTTP_CURRENT_USER_IE_PROXY_CONFIG</b> structure contains the Internet Explorer proxy configuration information.

## -struct-fields

### -field fAutoDetect

If TRUE, indicates that the Internet Explorer proxy configuration for the current user specifies "automatically detect settings".

### -field lpszAutoConfigUrl

Pointer to a null-terminated Unicode string that contains the auto-configuration URL if the Internet Explorer proxy configuration for the current user specifies "Use automatic proxy configuration".

### -field lpszProxy

Pointer to a null-terminated Unicode string that contains the proxy URL if the Internet Explorer proxy configuration for the current user specifies "use a proxy server".

### -field lpszProxyBypass

Pointer to a null-terminated Unicode string that contains the optional proxy by-pass server list.

## -see-also

<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP
		  Versions</a>