---
UID: NS:winhttp._WINHTTP_SECURITY_INFO
title: WINHTTP_SECURITY_INFO
ms.date: 11/4/2019
targetos: Windows
description: The WINHTTP_SECURITY_INFO structure contains a variety of timing information for an HTTP request.
tech.root: winhttp
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winhttp.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: WINHTTP_SECURITY_INFO, *PWINHTTP_SECURITY_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - _WINHTTP_SECURITY_INFO
 - WINHTTP_SECURITY_INFO
f1_keywords:
 - _WINHTTP_SECURITY_INFO
 - winhttp/_WINHTTP_SECURITY_INFO
 - PWINHTTP_SECURITY_INFO
 - winhttp/PWINHTTP_SECURITY_INFO
 - WINHTTP_SECURITY_INFO
 - winhttp/WINHTTP_SECURITY_INFO
dev_langs:
 - c++
---

## -description

The **WINHTTP_SECURITY_INFO** structure contains the SChannel connection and cipher information for a request.

## -struct-fields

### -field ConnectionInfo

[**SecPkgContext_ConnectionInfo**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo) containing the SChannel connection information for the request.

### -field CipherInfo

[**SecPkgContext_CipherInfo**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_cipherinfo) containing the SChannel cipher information for the request.

## -remarks

This structure is used with [**WinHttpQueryOption**](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve security information for a request by specifying the **WINHTTP_OPTION_SECURITY_INFO** flag.

## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)

