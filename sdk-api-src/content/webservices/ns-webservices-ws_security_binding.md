---
UID: NS:webservices._WS_SECURITY_BINDING
title: WS_SECURITY_BINDING (webservices.h)
description: The abstract base type for all security bindings.
helpviewer_keywords: ["WS_SECURITY_BINDING","WS_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_SECURITY_BINDING","wsw.ws_security_binding"]
old-location: wsw\ws_security_binding.htm
tech.root: wsw
ms.assetid: 6c0663e8-ae73-41a2-9273-50f53534926b
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_BINDING, WS_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_SECURITY_BINDING, wsw.ws_security_binding
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
req.typenames: WS_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_BINDING
 - webservices/_WS_SECURITY_BINDING
 - WS_SECURITY_BINDING
 - webservices/WS_SECURITY_BINDING
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
 - WS_SECURITY_BINDING
---

# WS_SECURITY_BINDING structure


## -description

The abstract base type for all security bindings.  One or more
concrete subtypes of this are specified in the 
<a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">security description</a> that is
supplied during channel and listener creation.  Each concrete subtype
of this corresponds to a security protocol and a way of using it to
provide authentication and/or protection to a channel.
            

Each security binding subtype instance in the security description
contributes one security token at runtime.  Thus, the fields of this
type can be viewed as specifying a security token, how to obtain it,
how to use it for channel security, and how to modify its behavior
using the optional settings.

## -struct-fields

### -field bindingType

The<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_type"> WS_SECURITY_BINDING_TYPE</a> of the security binding being described.  The type value
indicates how to obtain the security token corresponding to this
security binding.

### -field properties

The array of properties specifying the optional security binding
settings.  Each <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_binding_property">WS_SECURITY_BINDING_PROPERTY</a> in the array is a key-value
pair and must use a key defined in <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_ID</a>.  This field can be <b>NULL</b>, and if
it is <b>NULL</b>, the default value will be used for each security token
setting.

### -field propertyCount

The count of elements in the properties array.