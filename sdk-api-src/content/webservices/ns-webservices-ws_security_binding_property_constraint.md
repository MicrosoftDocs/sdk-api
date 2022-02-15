---
UID: NS:webservices._WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
title: WS_SECURITY_BINDING_PROPERTY_CONSTRAINT (webservices.h)
description: This structure is used to specify a set of constraints for a particular security binding property. Any property constraints that are not specified will use the default constraints.
helpviewer_keywords: ["WS_SECURITY_BINDING_PROPERTY_CONSTRAINT","WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure [Web Services for Windows]","webservices/WS_SECURITY_BINDING_PROPERTY_CONSTRAINT","wsw.ws_security_binding_property_constraint"]
old-location: wsw\ws_security_binding_property_constraint.htm
tech.root: wsw
ms.assetid: 97334ced-315d-49db-9c7b-b05ef387f6c8
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_BINDING_PROPERTY_CONSTRAINT, WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure [Web Services for Windows], webservices/WS_SECURITY_BINDING_PROPERTY_CONSTRAINT, wsw.ws_security_binding_property_constraint
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
req.typenames: WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
 - webservices/_WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
 - WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
 - webservices/WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
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
 - WS_SECURITY_BINDING_PROPERTY_CONSTRAINT
---

# WS_SECURITY_BINDING_PROPERTY_CONSTRAINT structure


## -description

This structure is used to specify a set of constraints
                for a particular security binding property.
                Any property constraints that are not specified will use
                the default constraints.

## -struct-fields

### -field id

The id of the security binding property.  The following security
                    binding property constraints may be specified:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a>
This property constraint may be specified when the
                      <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_constraint_type">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE</a> security binding is specified.
                    

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_constraint_type">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                        of <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_node_type">WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</a> will be used.
                    

</li>
</ul>

### -field allowedValues

An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the security binding property.  See the documentation for
                    a particular security binding property to determine the type of the
                    property.

### -field allowedValuesSize

The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    fields of the property structure will be filled out as follows:

### -field out.securityBindingProperty