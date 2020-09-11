---
UID: NS:webservices._WS_HOST_NAMES
title: WS_HOST_NAMES (webservices.h)
description: A structure containing a list of host names.
helpviewer_keywords: ["WS_HOST_NAMES","WS_HOST_NAMES structure [Web Services for Windows]","webservices/WS_HOST_NAMES","wsw.ws_host_names"]
old-location: wsw\ws_host_names.htm
tech.root: wsw
ms.assetid: 9815eb1e-0ce6-4b56-9f9a-e3938d502b72
ms.date: 12/05/2018
ms.keywords: WS_HOST_NAMES, WS_HOST_NAMES structure [Web Services for Windows], webservices/WS_HOST_NAMES, wsw.ws_host_names
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_HOST_NAMES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HOST_NAMES
 - webservices/_WS_HOST_NAMES
 - WS_HOST_NAMES
 - webservices/WS_HOST_NAMES
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
 - WS_HOST_NAMES
---

# WS_HOST_NAMES structure


## -description

A structure containing a list of host names.

## -struct-fields

### -field hostNames

A list of host names.  Each host name can be a DNS name or
                    an IPv4 or IPv6 address.  IPv6 addresses are enclosed
                    in brackets ('[' address ']').

### -field hostNameCount

The number of elements in the hostNames array.

