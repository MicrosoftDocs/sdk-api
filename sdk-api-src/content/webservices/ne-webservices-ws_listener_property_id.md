---
UID: NE:webservices.WS_LISTENER_PROPERTY_ID
title: WS_LISTENER_PROPERTY_ID
author: windows-sdk-content
description: Each listener property is of type WS_LISTENER_PROPERTY, is identified by an ID, and has an associated value. If a property is not specified when the listener is created, then its default value is used.
old-location: wsw\ws_listener_property_id.htm
old-project: wsw
ms.assetid: 4998d538-628f-4939-9db9-612e882e68b1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_LISTENER_PROPERTY_ASYNC_CALLBACK_MODEL, WS_LISTENER_PROPERTY_CHANNEL_BINDING, WS_LISTENER_PROPERTY_CHANNEL_TYPE, WS_LISTENER_PROPERTY_CLOSE_TIMEOUT, WS_LISTENER_PROPERTY_CONNECT_TIMEOUT, WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS, WS_LISTENER_PROPERTY_CUSTOM_LISTENER_INSTANCE, WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS, WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT, WS_LISTENER_PROPERTY_ID, WS_LISTENER_PROPERTY_ID enumeration [Web Services for Windows], WS_LISTENER_PROPERTY_IP_VERSION, WS_LISTENER_PROPERTY_IS_MULTICAST, WS_LISTENER_PROPERTY_LISTEN_BACKLOG, WS_LISTENER_PROPERTY_MULTICAST_INTERFACES, WS_LISTENER_PROPERTY_MULTICAST_LOOPBACK, WS_LISTENER_PROPERTY_STATE, WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS, WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS, webservices/WS_LISTENER_PROPERTY_ASYNC_CALLBACK_MODEL, webservices/WS_LISTENER_PROPERTY_CHANNEL_BINDING, webservices/WS_LISTENER_PROPERTY_CHANNEL_TYPE, webservices/WS_LISTENER_PROPERTY_CLOSE_TIMEOUT, webservices/WS_LISTENER_PROPERTY_CONNECT_TIMEOUT, webservices/WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS, webservices/WS_LISTENER_PROPERTY_CUSTOM_LISTENER_INSTANCE, webservices/WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS, webservices/WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT, webservices/WS_LISTENER_PROPERTY_ID, webservices/WS_LISTENER_PROPERTY_IP_VERSION, webservices/WS_LISTENER_PROPERTY_IS_MULTICAST, webservices/WS_LISTENER_PROPERTY_LISTEN_BACKLOG, webservices/WS_LISTENER_PROPERTY_MULTICAST_INTERFACES, webservices/WS_LISTENER_PROPERTY_MULTICAST_LOOPBACK, webservices/WS_LISTENER_PROPERTY_STATE, webservices/WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS, webservices/WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS, wsw.ws_listener_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WS_LISTENER_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_LISTENER_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_LISTENER_PROPERTY_ID enumeration


## -description


Each listener property is of type <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a>, is identified by an ID, and has an associated value.  If a property
                is not specified when the listener is created, then its default value is used.
            


## -enum-fields




### -field WS_LISTENER_PROPERTY_LISTEN_BACKLOG

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a>.  
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>ULONG</b>.

This controls the maximum length of the queue of pending connections. If set to 
                    SOMAXCONN, the backlog will be set to a maximum reasonable value. 
                


### -field WS_LISTENER_PROPERTY_IP_VERSION

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> or <b>WS_UDP_CHANNEL_BINDING</b>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is an <a href="https://msdn.microsoft.com/40e6d76a-4ac5-4759-ae82-6bbb482adae2">WS_IP_VERSION</a> value.

This property specifies which IP version that the listener should use.
                

The default value is <a href="https://msdn.microsoft.com/40e6d76a-4ac5-4759-ae82-6bbb482adae2">WS_IP_VERSION_AUTO</a>.
                


### -field WS_LISTENER_PROPERTY_STATE

Used with <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> for all channel types.
                    
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> value.

Returns the current <a href="https://msdn.microsoft.com/275d0d36-f9a1-49a7-af74-e8967dff574a">WS_LISTENER_STATE</a> of the listener.  The returned value is a snapshot of the current state, so it is
                    possible that the state may have changed before the caller has
                    had a chance to examine the value.
                


### -field WS_LISTENER_PROPERTY_ASYNC_CALLBACK_MODEL

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> for all channel types.
                    

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_CALLBACK_MODEL</a> value.

This value indicates the preferred async callback model when issuing
                    async operations for the listener or channels that are created for it
                    using <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                

The default is <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_LONG_CALLBACK</a>. 
                

The <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a> only supports <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">WS_LONG_CALLBACK</a> as an acceptable value
                    for this property.
                


### -field WS_LISTENER_PROPERTY_CHANNEL_TYPE

Used with <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> for all channel types.  

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE</a> value.

This property
                    specifies the message exchange pattern of the channel being used.
                


### -field WS_LISTENER_PROPERTY_CHANNEL_BINDING

Used with <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a> for all channel types.  

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CHANNEL_BINDING</a> value.

This property
                    specifies the binding of the channel being used.
                


### -field WS_LISTENER_PROPERTY_CONNECT_TIMEOUT

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> and   <b>WS_NAMEDPIPE_CHANNEL_BINDING</b>.

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>ULONG</b>.

An accept operation will wait
                    for an infinite amount of time to accept the underlying TCP socket or named pipe.  This
                    timeout corresponds to the amount of time dedicated to the net.tcp or net.pipe handshake
                    that takes place between the client and service once the client connects.
                    The timeout value is in milliseconds, where the value INFINITE indicates
                    no timeout.  Use the
                    <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_CONNECT_TIMEOUT</a> to set the corresponding
                    value on the client side.
                

The default value is 15000 (15 seconds).
                


### -field WS_LISTENER_PROPERTY_IS_MULTICAST

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_UDP_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_DUPLEX</a>to indicate that the listener is listening on a multicast address.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>BOOL</b>.

Note that setting this property is not sufficient when listening on
                    a multicast address.  The set of interfaces must also be specified
                    using the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_MULTICAST_INTERFACES</a>property.
                

The channel does not validate that the address is in fact a
                    a multicast address, but it sets the reuse of the socket 
                    such that another process can also open the same port.
                

The default value is <b>FALSE</b>.
                


### -field WS_LISTENER_PROPERTY_MULTICAST_INTERFACES

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/5c494651-3944-4424-8cd4-a6e14c239e80">WsSetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_UDP_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_DUPLEX</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is an array of <b>ULONG</b> values.

The size of the property
                    is sizeof(ULONG) multiplied by the number of values.  Each value represents
                    the interface index of an adapter.  The indices of adapters can be
                    obtained using the GetAdaptersAddresses function.
                

This value of the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_IS_MULTICAST</a> 
                    property must be <b>TRUE</b> in order to use this property.
                

The default value is an empty list (no interfaces).
                


### -field WS_LISTENER_PROPERTY_MULTICAST_LOOPBACK

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_UDP_CHANNEL_BINDING</a> 
                    with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_DUPLEX</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>BOOL</b>.

This indicates whether or not messages
                    sent on the loopback interface are received by this channel.  If <b>TRUE</b>,
                    then messages are received (otherwise, they will not be seen by the channel).
                

This value of the <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_IS_MULTICAST</a> 
                    property must be <b>TRUE</b> in order to use this property.
                

The default value is <b>TRUE</b>.
                


### -field WS_LISTENER_PROPERTY_CLOSE_TIMEOUT

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> or <a href="https://msdn.microsoft.com/cc4fb48a-8282-471a-aed0-1ca3134f9bd0">WsGetListenerProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> with <a href="https://msdn.microsoft.com/7e1092f9-10e8-485c-a286-770e1c74d8ca">WS_CHANNEL_TYPE_REPLY</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>ULONG</b>.

This indicates the number of milliseconds to
                    wait for clients to receive data from responses when <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a>is called.
                

The purpose of this timeout is to allow clients time to continue receiving 
                    data from HTTP responses sent by the server before the HTTP server disconnects
                    the client connections.
                

The calculation of the timeout value used is as follows:
                

<ul>
<li>At the time that <a href="https://msdn.microsoft.com/6023595a-ac52-4619-a824-df49da887fc5">WsCloseListener</a> is called, determine the
                    time the last response was sent (the last response time).  For the purposes of
                    this timeout calculation, a response is recorded as sent once <a href="https://msdn.microsoft.com/329193a7-932a-46d0-8e46-eef6bbdb8fa2">WsWriteMessageEnd</a>has been called for the response.  
                    </li>
<li>Calculate the difference between the current time and the last response time.
                    </li>
<li>If the difference is more than the timeout value, then the actual
                    timeout used is zero.
                    </li>
<li>If the difference is less than or equal to the timeout value, then the
                    actual timeout used is the timeout value minus the difference.
                </li>
</ul>
The default timeout value is 5000 (5 seconds).
                


### -field WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a>,
                    <b>WS_HTTP_CHANNEL_BINDING</b>, <b>WS_UDP_CHANNEL_BINDING</b>, or <b>WS_NAMEDPIPE_CHANNEL_BINDING</b>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>ULONG</b>.

The property value contains a set of flags (see <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_URL_MATCHING_OPTIONS</a>) which
                    specify how to match the URL in the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_TO_HEADER</a> of any received messages.
                

The default value is:
                

<pre class="syntax" xml:space="preserve"><code>
WS_MATCH_URL_THIS_HOST |
WS_MATCH_URL_EXACT_PATH |
WS_MATCH_URL_PORT |
WS_MATCH_URL_NO_QUERY
</code></pre>

### -field WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a> or
                    <b>WS_HTTP_CHANNEL_BINDING</b>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <b>ULONG</b>.

The property value contains a set of flags (see <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_URL_MATCHING_OPTIONS</a>) which
                    specify how to match the transport URL of any accepted channels.  See
                    <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_TRANSPORT_URL</a> for more information on the transport URL.
                

The default value is:
                

<pre class="syntax" xml:space="preserve"><code>
WS_MATCH_URL_THIS_HOST |
WS_MATCH_URL_EXACT_PATH |
WS_MATCH_URL_PORT |
WS_MATCH_URL_NO_QUERY
</code></pre>
This property only controls the verification of the message once it has been received
                    by the process, not the routing of the message to the process (which is determined
                    by the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>).                    
                


### -field WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a <a href="https://msdn.microsoft.com/b0be530f-5eff-4daa-90be-f9be648dfad7">WS_CUSTOM_LISTENER_CALLBACKS</a> structure.

This property is used to specify callbacks that
                    define the implementation of a custom listener.
                

This property must be specified when <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>is used.
                


### -field WS_LISTENER_PROPERTY_CUSTOM_LISTENER_PARAMETERS

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a pointer to an arbitrary sized data type.
                    The size of the property is the size of the data type.
                

This property is used to specify parameters used to create the custom
                    listener implementation.
                

The value of this property will be passed to the
                    <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                

If this property is not specified, it's value is <b>NULL</b> and size is zero.
                


### -field WS_LISTENER_PROPERTY_CUSTOM_LISTENER_INSTANCE

Used with <a href="https://msdn.microsoft.com/6f3440d2-90cc-4312-bb08-51f08b864cc7">WsGetChannelProperty</a>for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_CUSTOM_CHANNEL_BINDING</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a void* and size the property is sizeof(void*).  

The value 
                    corresponds to the listenerInstance value returned by the 
                    <a href="https://msdn.microsoft.com/2d8e476d-dc68-44b4-b53b-be440a32efda">WS_CREATE_LISTENER_CALLBACK</a>.
                

This property can be used to obtain the underlying listener
                    instance for a custom listener.  This allows a caller to directly
                    interact with the instance for cases when the existing
                    set of listener properties or listener functions is insufficient.
                


### -field WS_LISTENER_PROPERTY_DISALLOWED_USER_AGENT

Used with <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a> for <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structure is a pointer to <a href="https://msdn.microsoft.com/3a37275b-11e6-484a-adc2-1e9503d1b309">WS_DISALLOWED_USER_AGENT_SUBSTRINGS</a> which specifies the list of disallowed user
                    agents sub-strings.
                    <ul>
<li>Upon receiving the HTTP request, the UserAgent header value is extracted.
                        </li>
<li>Each sub-string in the list, is searched in the extracted UserAgent string value.
                        </li>
<li>If the substring is found the request is rejected.
                    </li>
</ul>


The list by default contains the following entry
                    <ul>
<li>Web Browser(s): Mozilla
                    </li>
</ul>


This property does not apply to listeners configured with <a href="https://msdn.microsoft.com/37858df7-ae76-41c1-8fd2-fc810b8927bf">WS_ENCODING_RAW</a> encoding.
                

