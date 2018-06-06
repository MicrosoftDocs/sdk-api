---
UID: NE:http._HTTP_AUTHENTICATION_HARDENING_LEVELS
title: "_HTTP_AUTHENTICATION_HARDENING_LEVELS"
author: windows-sdk-content
description: Server Hardening level.
old-location: http\http_authentication_hardening_levels.htm
old-project: Http
ms.assetid: da61e548-388a-4cb7-81bf-30bd312e27a6
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HTTP_AUTHENTICATION_HARDENING_LEVELS, HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration [HTTP], HttpAuthenticationHardeningLegacy, HttpAuthenticationHardeningMedium, HttpAuthenticationHardeningStrict, _HTTP_AUTHENTICATION_HARDENING_LEVELS, http.http_authentication_hardening_levels, http/HTTP_AUTHENTICATION_HARDENING_LEVELS, http/HttpAuthenticationHardeningLegacy, http/HttpAuthenticationHardeningMedium, http/HttpAuthenticationHardeningStrict
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: HTTP_AUTHENTICATION_HARDENING_LEVELS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_AUTHENTICATION_HARDENING_LEVELS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_AUTHENTICATION_HARDENING_LEVELS enumeration


## -description


Server Hardening level.


## -enum-fields




### -field HttpAuthenticationHardeningLegacy

Server is not hardened and operates without Channel Binding Token (CBT) support. 


### -field HttpAuthenticationHardeningMedium

Server is partially hardened.  Clients that support CBT are serviced appropriately.  Legacy clients are also serviced.


### -field HttpAuthenticationHardeningStrict

Server is hardened.  Only clients that supported CBT are serviced.

