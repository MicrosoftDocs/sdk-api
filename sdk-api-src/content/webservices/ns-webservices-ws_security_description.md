---
UID: NS:webservices._WS_SECURITY_DESCRIPTION
title: WS_SECURITY_DESCRIPTION (webservices.h)
description: The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).
helpviewer_keywords: ["WS_SECURITY_DESCRIPTION","WS_SECURITY_DESCRIPTION structure [Web Services for Windows]","webservices/WS_SECURITY_DESCRIPTION","wsw.ws_security_description"]
old-location: wsw\ws_security_description.htm
tech.root: wsw
ms.assetid: b9490f00-877c-4d9f-b361-eaca343cdee0
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_DESCRIPTION, WS_SECURITY_DESCRIPTION structure [Web Services for Windows], webservices/WS_SECURITY_DESCRIPTION, wsw.ws_security_description
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
req.typenames: WS_SECURITY_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_DESCRIPTION
 - webservices/_WS_SECURITY_DESCRIPTION
 - WS_SECURITY_DESCRIPTION
 - webservices/WS_SECURITY_DESCRIPTION
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
 - WS_SECURITY_DESCRIPTION
---

# WS_SECURITY_DESCRIPTION structure


## -description

The top-level structure used to specify the security requirements for
a <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">channel</a> (on the client side) or a <a href="/windows/desktop/api/webservices/nf-webservices-wscreatelistener">listener</a> (on the server side).

## -struct-fields

### -field securityBindings

The array of pointers to security bindings.  The set of security
bindings supplies determines the kind of security applied to the
channel.  Each security binding specifies one security token.

### -field securityBindingCount

The count of elements in the securityBindings array.

### -field properties

The array of properties specifying the optional channel-wide security
settings.  Each <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_property">WS_SECURITY_PROPERTY</a> in the array is a key-value
pair and must use a key defined in <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_ID</a>.  This field can be <b>NULL</b>,
and if it is <b>NULL</b>, the default value will be used for each security
channel setting.

### -field propertyCount

The count of elements in the properties array.

## -remarks

The figure below illustrates the structure of a security description.

:::image type="content" source="images/SecurityDescription.png" border="false" alt-text="Diagram of the elements in a security description. A Channel-wide Settings Bag,  a Security Binding, and the properties of the Security Binding.":::
