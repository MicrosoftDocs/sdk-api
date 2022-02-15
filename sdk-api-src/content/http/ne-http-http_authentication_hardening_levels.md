---
UID: NE:http._HTTP_AUTHENTICATION_HARDENING_LEVELS
title: HTTP_AUTHENTICATION_HARDENING_LEVELS (http.h)
description: Server Hardening level.
helpviewer_keywords: ["HTTP_AUTHENTICATION_HARDENING_LEVELS","HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration [HTTP]","HttpAuthenticationHardeningLegacy","HttpAuthenticationHardeningMedium","HttpAuthenticationHardeningStrict","http.http_authentication_hardening_levels","http/HTTP_AUTHENTICATION_HARDENING_LEVELS","http/HttpAuthenticationHardeningLegacy","http/HttpAuthenticationHardeningMedium","http/HttpAuthenticationHardeningStrict"]
old-location: http\http_authentication_hardening_levels.htm
tech.root: http
ms.assetid: da61e548-388a-4cb7-81bf-30bd312e27a6
ms.date: 12/05/2018
ms.keywords: HTTP_AUTHENTICATION_HARDENING_LEVELS, HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration [HTTP], HttpAuthenticationHardeningLegacy, HttpAuthenticationHardeningMedium, HttpAuthenticationHardeningStrict, http.http_authentication_hardening_levels, http/HTTP_AUTHENTICATION_HARDENING_LEVELS, http/HttpAuthenticationHardeningLegacy, http/HttpAuthenticationHardeningMedium, http/HttpAuthenticationHardeningStrict
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_AUTHENTICATION_HARDENING_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_AUTHENTICATION_HARDENING_LEVELS
 - http/_HTTP_AUTHENTICATION_HARDENING_LEVELS
 - HTTP_AUTHENTICATION_HARDENING_LEVELS
 - http/HTTP_AUTHENTICATION_HARDENING_LEVELS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_AUTHENTICATION_HARDENING_LEVELS
---

# HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration


## -description

Server Hardening level.

## -enum-fields

### -field HttpAuthenticationHardeningLegacy:0

Server is not hardened and operates without Channel Binding Token (CBT) support.

### -field HttpAuthenticationHardeningMedium

Server is partially hardened.  Clients that support CBT are serviced appropriately.  Legacy clients are also serviced.

### -field HttpAuthenticationHardeningStrict

Server is hardened.  Only clients that supported CBT are serviced.

