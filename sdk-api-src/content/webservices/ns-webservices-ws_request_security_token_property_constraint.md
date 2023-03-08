---
UID: NS:webservices._WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
title: WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT (webservices.h)
description: This structure is used to specify a set of constraints for a particular request security token property. Any property constraints that are not specified will use the default constraints.
helpviewer_keywords: ["WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT","WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT structure [Web Services for Windows]","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT","wsw.ws_request_security_token_property_constraint"]
old-location: wsw\ws_request_security_token_property_constraint.htm
tech.root: wsw
ms.assetid: 96bd488f-ef28-402a-ae55-a30416f4e103
ms.date: 12/05/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT, WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT structure [Web Services for Windows], webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT, wsw.ws_request_security_token_property_constraint
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
req.typenames: WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
 - webservices/_WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
 - WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
 - webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
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
 - WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT
---

# WS_REQUEST_SECURITY_TOKEN_PROPERTY_CONSTRAINT structure


## -description

This structure is used to specify a set of constraints
                for a particular request security token property.
                Any property constraints that are not specified will use
                the default constraints.

## -struct-fields

### -field id

The id of the request security token property.  The following security
                    property constraint may be specified:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_property_id">WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION</a>
This property indicates which WS-Trust versions are acceptable.
                    

If this property is not specified, then the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION_FEBRUARY_2005</a> will be used.
                    

Currently only <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION_FEBRUARY_2005</a> is supported in policy, so a property constraint containing the
                        value <b>WS_TRUST_VERSION_FEBRUARY_2005</b> must be specified in
                        order for the policy to match.
                    

</li>
</ul>

### -field allowedValues

An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the request security token property.  See the documentation for
                    a particular request security token property to determine the type of the
                    property.

### -field allowedValuesSize

The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.

### -field out.requestSecurityTokenProperty