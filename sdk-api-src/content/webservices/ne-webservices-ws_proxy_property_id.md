---
UID: NE:webservices.__unnamed_enum_97
title: WS_PROXY_PROPERTY_ID (webservices.h)
description: Optional parameters for configuring the service proxy. With an exception of WS_PROXY_PROPERTY_STATE all the values are only supported for use with WsCreateServiceProxy as part of the WS_PROXY_PROPERTY* parameter.
helpviewer_keywords: ["WS_PROXY_FAULT_LANG_ID","WS_PROXY_PROPERTY_CALL_TIMEOUT","WS_PROXY_PROPERTY_ID","WS_PROXY_PROPERTY_ID enumeration [Web Services for Windows]","WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE","WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT","WS_PROXY_PROPERTY_MAX_PENDING_CALLS","WS_PROXY_PROPERTY_MESSAGE_PROPERTIES","WS_PROXY_PROPERTY_STATE","webservices/WS_PROXY_FAULT_LANG_ID","webservices/WS_PROXY_PROPERTY_CALL_TIMEOUT","webservices/WS_PROXY_PROPERTY_ID","webservices/WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE","webservices/WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT","webservices/WS_PROXY_PROPERTY_MAX_PENDING_CALLS","webservices/WS_PROXY_PROPERTY_MESSAGE_PROPERTIES","webservices/WS_PROXY_PROPERTY_STATE","wsw.ws_proxy_property_id"]
old-location: wsw\ws_proxy_property_id.htm
tech.root: wsw
ms.assetid: d81944ae-74b9-4eee-b02f-5b1d5c99c358
ms.date: 12/05/2018
ms.keywords: WS_PROXY_FAULT_LANG_ID, WS_PROXY_PROPERTY_CALL_TIMEOUT, WS_PROXY_PROPERTY_ID, WS_PROXY_PROPERTY_ID enumeration [Web Services for Windows], WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE, WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT, WS_PROXY_PROPERTY_MAX_PENDING_CALLS, WS_PROXY_PROPERTY_MESSAGE_PROPERTIES, WS_PROXY_PROPERTY_STATE, webservices/WS_PROXY_FAULT_LANG_ID, webservices/WS_PROXY_PROPERTY_CALL_TIMEOUT, webservices/WS_PROXY_PROPERTY_ID, webservices/WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE, webservices/WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT, webservices/WS_PROXY_PROPERTY_MAX_PENDING_CALLS, webservices/WS_PROXY_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_PROXY_PROPERTY_STATE, wsw.ws_proxy_property_id
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
req.typenames: WS_PROXY_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_PROXY_PROPERTY_ID
 - webservices/WS_PROXY_PROPERTY_ID
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
 - WS_PROXY_PROPERTY_ID
---

# WS_PROXY_PROPERTY_ID enumeration


## -description

Optional parameters for configuring the service proxy. With an exception of
                <b>WS_PROXY_PROPERTY_STATE</b> all the values are only supported for 
                use with <a href="/windows/desktop/api/webservices/nf-webservices-wscreateserviceproxy">WsCreateServiceProxy</a> as part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_proxy_property">WS_PROXY_PROPERTY*</a> parameter.

## -enum-fields

### -field WS_PROXY_PROPERTY_CALL_TIMEOUT:0

The maximum amount of time in milliseconds for a call to remain pending. 
                    Default is 30000 milliseconds(30 seconds).  It is of type <b>ULONG</b>.

If an application wishes to have no timeout associated with a call, it can set the value to INFINITE.
                

This property is write only.

### -field WS_PROXY_PROPERTY_MESSAGE_PROPERTIES:1

This property allows the user to specify properties of the message
                    objects used by the service proxy to send and receive messages.
                

This property may be specified when the service proxy is created.
                

The value specified should be of type <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_properties">WS_MESSAGE_PROPERTIES</a>.
                

The following message properties may be specified:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_HEAP_PROPERTIES</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS</a>
</li>
</ul>

### -field WS_PROXY_PROPERTY_MAX_CALL_POOL_SIZE:2

Each call in the service proxy is represented by an object internal to the service proxy. 
                    A call object is designed such that after every call it can be reused. 
                    This allows applications to scale better in scenarios where they expect 
                    large number of calls over the service proxy. The default value for this property is 5.
                 It is of type <b>USHORT</b>.

This property is write only.

### -field WS_PROXY_PROPERTY_STATE:3

The current state of the service proxy.
                It is of type <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_proxy_state">WS_SERVICE_PROXY_STATE</a>.

This property is read only.
                

The returned value is a snapshot of the current state, so it is
                    possible that the state may have changed before the caller has
                    had a chance to examine the value.

### -field WS_PROXY_PROPERTY_MAX_PENDING_CALLS:4

The maximum number of pending calls allowed on the service proxy. If the 
                    maximum number of calls pending on the service proxy reaches this limit, the
                    incoming calls will be rejected with <b>WS_E_QUOTA_EXCEEDED</b> (see <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>). The default value 
                    for this property is 100.
                 It is of type <b>ULONG</b>.

This property is write only.

### -field WS_PROXY_PROPERTY_MAX_CLOSE_TIMEOUT:5

The amount of time in milliseconds the service proxy will wait for the pending calls to complete.
                    Once the timeout expires, the service proxy will abort itself.
                

The default value for this property is 5000 (5 seconds).
                

This property is write only.
                 It is of type <b>ULONG</b>.

### -field WS_PROXY_FAULT_LANG_ID:6

The LANGID that would be used for returning a fault. If none specified default user locale will be used. It is of type <a href="/windows/desktop/Intl/language-identifiers">LANGID</a>. 
                

This property is write only.
