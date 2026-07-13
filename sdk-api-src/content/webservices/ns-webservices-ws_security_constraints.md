---
UID: NS:webservices._WS_SECURITY_CONSTRAINTS
title: WS_SECURITY_CONSTRAINTS (webservices.h)
description: This structure specifies the security related constraints as part of WS_POLICY_CONSTRAINTS.
helpviewer_keywords: ["WS_SECURITY_CONSTRAINTS","WS_SECURITY_CONSTRAINTS structure [Web Services for Windows]","webservices/WS_SECURITY_CONSTRAINTS","wsw.ws_security_constraints"]
old-location: wsw\ws_security_constraints.htm
tech.root: wsw
ms.assetid: 17fe7602-c050-46a2-b55c-aac6c277a5ce
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_CONSTRAINTS, WS_SECURITY_CONSTRAINTS structure [Web Services for Windows], webservices/WS_SECURITY_CONSTRAINTS, wsw.ws_security_constraints
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
req.typenames: WS_SECURITY_CONSTRAINTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_CONSTRAINTS
 - webservices/_WS_SECURITY_CONSTRAINTS
 - WS_SECURITY_CONSTRAINTS
 - webservices/WS_SECURITY_CONSTRAINTS
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
 - WS_SECURITY_CONSTRAINTS
---

# WS_SECURITY_CONSTRAINTS structure


## -description

This structure specifies the security related constraints
                as part of <a href="/windows/desktop/api/webservices/ns-webservices-ws_policy_constraints">WS_POLICY_CONSTRAINTS</a>.

## -struct-fields

### -field securityPropertyConstraints

An array of security property constraints which override the default
                    set of constraints.  The constraints specified here, combined
                    with the default set of constraints limits the set of policies
                    that will be matched.
                

If a security property constraint is not specified for a given property,
                    then a default constraint value will be used.
                    See <a href="/windows/win32/api/webservices/ns-webservices-ws_security_property_constraint">WS_SECURITY_PROPERTY_CONSTRAINT</a> for the
                    supported set of properties and their default values.
                

Note that the defaults constraints for <a href="/windows/win32/api/webservices/ns-webservices-ws_security_property_constraint">WS_SECURITY_PROPERTY_CONSTRAINT</a> 
                    are the same as the defaults for <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_property">WS_SECURITY_PROPERTY</a>.

### -field securityPropertyConstraintCount

The number of elements specified in the securityPropertyConstraints
                    array.
                

If this value is 0, then the securityPropertyConstraints array may be <b>NULL</b>.

### -field securityBindingConstraints

Any array of security binding constraints which taken as a unit specify
                    the type of security to match in the policy.
                

The type of each <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> corresponds
                    to the types of security that is specified using a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_binding">WS_SECURITY_BINDING</a> structure.  Each security binding specifies one security token, and similarly,
                    each security binding constraint specifies constraints on one security token.
                

Specifying zero constraints indicates no security.

### -field securityBindingConstraintCount

The number of elements specified in the securityBindingConstraints
                    array.
                

If this value is 0, then the securityBindingConstraints array may be <b>NULL</b>.