---
UID: NS:webservices._WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
title: WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT (webservices.h)
description: A security binding constraint that can be used to extract information about how to obtain an issued token from an issuing party.
helpviewer_keywords: ["WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT","WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows]","webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT","wsw.ws_issued_token_message_security_binding_constraint"]
old-location: wsw\ws_issued_token_message_security_binding_constraint.htm
tech.root: wsw
ms.assetid: 7588f526-d1d5-486f-b317-f1a4b35e3882
ms.date: 12/05/2018
ms.keywords: WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT, WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT, wsw.ws_issued_token_message_security_binding_constraint
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
req.typenames: WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - webservices/_WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
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
 - WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT
---

# WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT structure


## -description

A security binding constraint that can be used to extract information
                about how to obtain an issued token from an issuing party.

## -struct-fields

### -field bindingConstraint

The base binding constraint that this binding constraint derives from.
                

There are currently no binding-specific properties defined for this binding constraint.

### -field bindingUsage

This specifies how the issued token should be attached to a message.

### -field claimConstraints

This field contains a list of claim types that 
                    are allowed in the policy.  Each claim type is 
                    a URI which identifies the type of claim.

### -field claimConstraintCount

The number of elements in the claimConstraints array.
                

If this value is 0, then the claimConstraints array may be
                    <b>NULL</b>, and any claims are allowed to appear in the policy.

### -field requestSecurityTokenPropertyConstraints

A set of property constraints relating to how to request a security token.
                

See <a href="/windows/win32/api/webservices/ns-webservices-ws_request_security_token_property_constraint">WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT</a> for more information.

### -field requestSecurityTokenPropertyConstraintCount

The number of elements in the requestSecurityTokenPropertyConstraints array.
                

If the array has zero elements, the requestSecurityTokenPropertyConstraints field may be <b>NULL</b>.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.

### -field out.issuerAddress

### -field out.requestSecurityTokenTemplate

## -remarks

The information extracted using this binding constraint can be used
                with <a href="/windows/desktop/api/webservices/nf-webservices-wsrequestsecuritytoken">WsRequestSecurityToken</a> to obtain an issued token.
                The issued token can then be used with the 
                <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> security binding.
            

This binding constraint is typically used in federated security
                scenarios.