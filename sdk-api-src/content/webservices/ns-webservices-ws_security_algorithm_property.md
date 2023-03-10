---
UID: NS:webservices._WS_SECURITY_ALGORITHM_PROPERTY
title: WS_SECURITY_ALGORITHM_PROPERTY (webservices.h)
description: Specifies a cryptographic algorithm setting.
helpviewer_keywords: ["WS_SECURITY_ALGORITHM_PROPERTY","WS_SECURITY_ALGORITHM_PROPERTY structure [Web Services for Windows]","webservices/WS_SECURITY_ALGORITHM_PROPERTY","wsw.ws_security_algorithm_property"]
old-location: wsw\ws_security_algorithm_property.htm
tech.root: wsw
ms.assetid: 6a0dbe45-65f6-41eb-aa94-5ed0cdd751cf
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_ALGORITHM_PROPERTY, WS_SECURITY_ALGORITHM_PROPERTY structure [Web Services for Windows], webservices/WS_SECURITY_ALGORITHM_PROPERTY, wsw.ws_security_algorithm_property
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_ALGORITHM_PROPERTY
 - webservices/_WS_SECURITY_ALGORITHM_PROPERTY
 - WS_SECURITY_ALGORITHM_PROPERTY
 - webservices/WS_SECURITY_ALGORITHM_PROPERTY
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
 - WS_SECURITY_ALGORITHM_PROPERTY
---

# WS_SECURITY_ALGORITHM_PROPERTY structure


## -description

Specifies a cryptographic algorithm setting.

## -struct-fields

### -field id

Identifies the <a href="/windows/win32/api/webservices/ne-webservices-ws_move_to">WS_SECURITY_ALGORITHM_PROPERTY_ID</a>.

### -field value

A pointer to the value to set.
                The pointer must have an alignment compatible with the type
                of the property.

### -field valueSize

The size in bytes of the memory pointed to by value.

