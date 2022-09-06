---
UID: NE:webservices.__unnamed_enum_106
title: WS_POLICY_PROPERTY_ID (webservices.h)
description: Identifies each policy property and its associated value.
helpviewer_keywords: ["WS_POLICY_PROPERTY_ID","WS_POLICY_PROPERTY_ID enumeration [Web Services for Windows]","WS_POLICY_PROPERTY_MAX_ALTERNATIVES","WS_POLICY_PROPERTY_MAX_DEPTH","WS_POLICY_PROPERTY_MAX_EXTENSIONS","WS_POLICY_PROPERTY_STATE","webservices/WS_POLICY_PROPERTY_ID","webservices/WS_POLICY_PROPERTY_MAX_ALTERNATIVES","webservices/WS_POLICY_PROPERTY_MAX_DEPTH","webservices/WS_POLICY_PROPERTY_MAX_EXTENSIONS","webservices/WS_POLICY_PROPERTY_STATE","wsw.ws_policy_property_id"]
old-location: wsw\ws_policy_property_id.htm
tech.root: wsw
ms.assetid: 503d39c0-7546-429d-b8e3-66e80c76b7c1
ms.date: 12/05/2018
ms.keywords: WS_POLICY_PROPERTY_ID, WS_POLICY_PROPERTY_ID enumeration [Web Services for Windows], WS_POLICY_PROPERTY_MAX_ALTERNATIVES, WS_POLICY_PROPERTY_MAX_DEPTH, WS_POLICY_PROPERTY_MAX_EXTENSIONS, WS_POLICY_PROPERTY_STATE, webservices/WS_POLICY_PROPERTY_ID, webservices/WS_POLICY_PROPERTY_MAX_ALTERNATIVES, webservices/WS_POLICY_PROPERTY_MAX_DEPTH, webservices/WS_POLICY_PROPERTY_MAX_EXTENSIONS, webservices/WS_POLICY_PROPERTY_STATE, wsw.ws_policy_property_id
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
req.typenames: WS_POLICY_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_POLICY_PROPERTY_ID
 - webservices/WS_POLICY_PROPERTY_ID
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
 - WS_POLICY_PROPERTY_ID
---

# WS_POLICY_PROPERTY_ID enumeration


## -description

Identifies each policy property and its associated
                value.

## -enum-fields

### -field WS_POLICY_PROPERTY_STATE:1

This property is used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetpolicyproperty">WsGetPolicyProperty</a>.
                 It is of type <a href="/windows/desktop/api/webservices/ne-webservices-ws_policy_state">WS_POLICY_STATE</a>.

The current state of the policy object.

### -field WS_POLICY_PROPERTY_MAX_ALTERNATIVES:2

This property is used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemetadata">WsCreateMetadata</a> when
                    specifying <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_property_id">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a> as part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_metadata_property">WS_METADATA_PROPERTY*</a> parameter.  It is of type <b>ULONG</b>.
                

This property controls the maximum number of alternatives
                    allowed for a given <a href="/windows/desktop/wsw/ws-policy">WS_POLICY</a> object.
                

When a policy is processed, the amount of memory allocated 
                    and CPU consumed is proportional to the number of policy
                    alternatives present in the policy, not to the actual size
                    of the policy.  Even a small policy may contain a large number
                    of alternatives due to the expansion of different permutations
                    of assertions.  Setting this property to a large
                    value may lead to excessive processing or memory consumption.
                

The default value is 32.

### -field WS_POLICY_PROPERTY_MAX_DEPTH:3

This property is used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemetadata">WsCreateMetadata</a> when
                    specifying <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_property_id">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a>.
                  It is of type <b>ULONG</b>.

This property controls the maximum depth of any policy that is
                    read and processed.  The maximum depth of a policy is defined as the maximum
                    number of levels of nested container elements (<b>Policy</b>, <b>All</b>, <b>ExactlyOne</b>)
                    when considering the policy and any policies that it references.
                

A small amount of stack space is consumed for each level of
                    policy that is processed.  Setting this value to a large
                    value may lead to stack overflow for a policy that is 
                    deeply nested or contains a cyclic reference.
                

The default value is 32.

### -field WS_POLICY_PROPERTY_MAX_EXTENSIONS:4

This property is used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemetadata">WsCreateMetadata</a> when
                    specifying <a href="/windows/desktop/api/webservices/ne-webservices-ws_metadata_property_id">WS_METADATA_PROPERTY_POLICY_PROPERTIES</a>.
                 It is of type <b>ULONG</b>.

This property controls the maximum number of policy extensions 
                    (unknown assertions) allowed for a given <a href="/windows/desktop/wsw/ws-policy">WS_POLICY</a> object. 
                    Policy extensions can be retrieved by supplying <a href="/windows/desktop/api/webservices/ns-webservices-ws_policy_extension">WS_POLICY_EXTENSION</a> 
                    array in <a href="/windows/desktop/api/webservices/ns-webservices-ws_policy_constraints">WS_POLICY_CONSTRAINTS</a> structure when using the 
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> API.
                

The default value is 8.
                

When a policy is processed, the amount of memory allocated 
                    and CPU consumed is proportional to the number of policy
                    alternatives present in the policy, not to the actual size
                    of the policy.  Even a small policy may contain a large number
                    of alternatives due to the expansion of different permutations
                    of assertions.  Setting this property to a large
                    value may lead to excessive processing or memory consumption.
