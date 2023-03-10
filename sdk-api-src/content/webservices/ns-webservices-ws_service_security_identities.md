---
UID: NS:webservices._WS_SERVICE_SECURITY_IDENTITIES
title: WS_SERVICE_SECURITY_IDENTITIES (webservices.h)
description: A list of Server Principal Names (SPNs) that are used to validate Extended Protection.
helpviewer_keywords: ["WS_SERVICE_SECURITY_IDENTITIES","WS_SERVICE_SECURITY_IDENTITIES structure [Web Services for Windows]","webservices/WS_SERVICE_SECURITY_IDENTITIES","wsw.ws_service_security_identities"]
old-location: wsw\ws_service_security_identities.htm
tech.root: wsw
ms.assetid: d38f0efd-2570-4db1-b4f7-113a45fe4449
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_SECURITY_IDENTITIES, WS_SERVICE_SECURITY_IDENTITIES structure [Web Services for Windows], webservices/WS_SERVICE_SECURITY_IDENTITIES, wsw.ws_service_security_identities
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_SERVICE_SECURITY_IDENTITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_SECURITY_IDENTITIES
 - webservices/_WS_SERVICE_SECURITY_IDENTITIES
 - WS_SERVICE_SECURITY_IDENTITIES
 - webservices/WS_SERVICE_SECURITY_IDENTITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_SECURITY_IDENTITIES
---

# WS_SERVICE_SECURITY_IDENTITIES structure


## -description

A list of Server Principal Names (SPNs) that are used to validate <a href="/windows/desktop/wsw/extended-protection">Extended Protection</a>. 
            

Only available on the server.

## -struct-fields

### -field serviceIdentities

A array of strings representing the SPNs accepted by the server. Wildcards are not allowed.

### -field serviceIdentityCount

The number of strings in serviceIdentities.