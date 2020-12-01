---
UID: NS:webservices._WS_CHANNEL_PROPERTY_CONSTRAINT
title: WS_CHANNEL_PROPERTY_CONSTRAINT (webservices.h)
description: Specifies constraints for a particular channel property.
helpviewer_keywords: ["WS_CHANNEL_PROPERTY_CONSTRAINT","WS_CHANNEL_PROPERTY_CONSTRAINT structure [Web Services for Windows]","webservices/WS_CHANNEL_PROPERTY_CONSTRAINT","wsw.ws_channel_property_constraint"]
old-location: wsw\ws_channel_property_constraint.htm
tech.root: wsw
ms.assetid: 548dcba5-dc78-402e-a930-a58fb462c08a
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_PROPERTY_CONSTRAINT, WS_CHANNEL_PROPERTY_CONSTRAINT structure [Web Services for Windows], webservices/WS_CHANNEL_PROPERTY_CONSTRAINT, wsw.ws_channel_property_constraint
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
req.typenames: WS_CHANNEL_PROPERTY_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CHANNEL_PROPERTY_CONSTRAINT
 - webservices/_WS_CHANNEL_PROPERTY_CONSTRAINT
 - WS_CHANNEL_PROPERTY_CONSTRAINT
 - webservices/WS_CHANNEL_PROPERTY_CONSTRAINT
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
 - WS_CHANNEL_PROPERTY_CONSTRAINT
---

# WS_CHANNEL_PROPERTY_CONSTRAINT structure


## -description

Specifies constraints
                for a particular channel property.Any property constraints that are not specified will use
                the default constraints.

## -struct-fields

### -field id

The ID of the channel property.  The following channel 
                    properties constraints may be specified:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ENCODING</a>
If this property constraint is not specified when using 
                        <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_encoding">WS_ENCODING_XML_UTF8</a> will be used.
                    

If this property constraint is not specified not specified when using 
                        <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_TCP_CHANNEL_BINDING</a> the default constraint value of 
                        <a href="/windows/desktop/api/webservices/ne-webservices-ws_encoding">WS_ENCODING_XML_BINARY_SESSION_1</a> will be used.
                    

</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ADDRESSING_VERSION</a>
If this property constraint is not specified, the default constraint
                        value of <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_1_0</a> will be used.
                    

</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_ENVELOPE_VERSION</a>
If this property constraint is not specified, the default constraint of 
                        value of <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_2</a> will be used.
                    

</li>
</ul>

### -field allowedValues

An array of acceptable values.  The type of
                    the values in the array correspond to the type of the values
                    of the channel property.  See the documentation for
                    a particular channel property to determine the type of the
                    property.

### -field allowedValuesSize

The total size of the <b>allowedValues</b> array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.

### -field out.channelProperty