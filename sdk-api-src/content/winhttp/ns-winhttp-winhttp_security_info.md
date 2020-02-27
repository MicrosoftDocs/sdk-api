---
UID: NS:winhttp._WINHTTP_SECURITY_INFO
title: WINHTTP_SECURITY_INFO (winhttp.h)
description: The WINHTTP_SECURITY_INFO structure contains a variety of timing information for an HTTP request.
old-location:
tech.root: WinHttp
ms.assetid: f4459d2c-de31-4313-ae26-b8f8c1c7b56b
ms.date: 02/25/2020
ms.keywords: '*LPWINHTTP_SECURITY_INFO, WINHTTP_SECURITY_INFO, WINHTTP_SECURITY_INFO structure [HTTP], http.winhttp_security_info, winhttp/WINHTTP_SECURITY_INFO, WINHTTP_OPTION_SECURITY_INFO'
f1_keywords:
- winhttp/WINHTTP_SECURITY_INFO
dev_langs:
- c++
req.header: winhttp.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 [desktop apps only]
req.target-min-winversvr: Windows Server Insider Preview [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winhttp.h
api_name:
- WINHTTP_SECURITY_INFO
targetos: Windows
req.typenames: WINHTTP_SECURITY_INFO, *LPWINHTTP_SECURITY_INFO
req.redist:
ms.custom: Vb
---

# WINHTTP_SECURITY_INFO structure


## -description

The **WINHTTP\_SECURITY\_INFO** structure contains the SChannel connection and cipher information for a request.


## -struct-fields


### -field ConnectionInfo

[**SecPkgContext\_ConnectionInfo**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo) containing the SChannel connection information for the request.


### -field CipherInfo

[**SecPkgContext\_CipherInfo**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_cipherinfo) containing the SChannel cipher information for the request.


## -remarks

This structure is used with [WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve security information for a request by specifying the **WINHTTP\_OPTION\_SECURITY\_INFO** flag.


## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)
