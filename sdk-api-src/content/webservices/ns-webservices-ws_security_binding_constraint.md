---
UID: NS:webservices._WS_SECURITY_BINDING_CONSTRAINT
title: WS_SECURITY_BINDING_CONSTRAINT (webservices.h)
description: The base class for all security binding constraint structures.
helpviewer_keywords: ["WS_SECURITY_BINDING_CONSTRAINT","WS_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows]","webservices/WS_SECURITY_BINDING_CONSTRAINT","wsw.ws_security_binding_constraint"]
old-location: wsw\ws_security_binding_constraint.htm
tech.root: wsw
ms.assetid: d79795ea-6780-4d13-9d40-bd1ea7cd5113
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_BINDING_CONSTRAINT, WS_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], webservices/WS_SECURITY_BINDING_CONSTRAINT, wsw.ws_security_binding_constraint
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
req.typenames: WS_SECURITY_BINDING_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_BINDING_CONSTRAINT
 - webservices/_WS_SECURITY_BINDING_CONSTRAINT
 - WS_SECURITY_BINDING_CONSTRAINT
 - webservices/WS_SECURITY_BINDING_CONSTRAINT
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
 - WS_SECURITY_BINDING_CONSTRAINT
---

# WS_SECURITY_BINDING_CONSTRAINT structure


## -description

The base class for all security binding constraint structures.

## -struct-fields

### -field type

This value depends on which type of security binding constraint that is used.

### -field propertyConstraints

A set of binding-specific security property constraints.
                

See <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_property_constraint">WS_SECURITY_BINDING_PROPERTY_CONSTRAINT</a> for more information.

### -field propertyConstraintCount

The number of elements in the propertyConstraints array.
                

If the array has zero elements, the propertyConstraints field may be <b>NULL</b>.

