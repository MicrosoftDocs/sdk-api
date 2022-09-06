---
UID: NE:webservices.__unnamed_enum_33
title: WS_FAULT_DISCLOSURE (webservices.h)
description: Controls how much error information is included in a fault. Since the error object may contain sensitive data as part of the error string, it is not always appropriate to include the error strings information in all faults.
helpviewer_keywords: ["WS_FAULT_DISCLOSURE","WS_FAULT_DISCLOSURE enumeration [Web Services for Windows]","WS_FULL_FAULT_DISCLOSURE","WS_MINIMAL_FAULT_DISCLOSURE","webservices/WS_FAULT_DISCLOSURE","webservices/WS_FULL_FAULT_DISCLOSURE","webservices/WS_MINIMAL_FAULT_DISCLOSURE","wsw.ws_fault_disclosure"]
old-location: wsw\ws_fault_disclosure.htm
tech.root: wsw
ms.assetid: 1dca9074-b329-4293-8a44-d0ced00ae59e
ms.date: 12/05/2018
ms.keywords: WS_FAULT_DISCLOSURE, WS_FAULT_DISCLOSURE enumeration [Web Services for Windows], WS_FULL_FAULT_DISCLOSURE, WS_MINIMAL_FAULT_DISCLOSURE, webservices/WS_FAULT_DISCLOSURE, webservices/WS_FULL_FAULT_DISCLOSURE, webservices/WS_MINIMAL_FAULT_DISCLOSURE, wsw.ws_fault_disclosure
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_FAULT_DISCLOSURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_FAULT_DISCLOSURE
 - webservices/WS_FAULT_DISCLOSURE
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
 - WS_FAULT_DISCLOSURE
---

# WS_FAULT_DISCLOSURE enumeration


## -description

Controls how much error information is included in a fault.
                Since the error object may contain sensitive
                data as part of the error string, it is not
                always appropriate to include the error strings
                information in all faults.

## -enum-fields

### -field WS_MINIMAL_FAULT_DISCLOSURE:0

Use a generic fault string for all errors.

### -field WS_FULL_FAULT_DISCLOSURE:1

Use the error string as the fault string.

