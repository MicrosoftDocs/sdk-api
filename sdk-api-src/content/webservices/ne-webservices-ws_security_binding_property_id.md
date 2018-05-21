---
UID: NE:webservices.WS_SECURITY_BINDING_PROPERTY_ID
title: WS_SECURITY_BINDING_PROPERTY_ID
author: windows-driver-content
description: Identifies the properties used to specify security binding settings. Security binding settings are present in security bindings that are used, in turn, in a security description.
old-location: wsw\ws_security_binding_property_id.htm
old-project: wsw
ms.assetid: 6c8b3277-3f49-469b-9783-c552a4c44558
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL, WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS, WS_SECURITY_BINDING_PROPERTY_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE, WS_SECURITY_BINDING_PROPERTY_DISABLE_CERT_REVOCATION_CHECK, WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_BASIC_REALM, WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_DOMAIN, WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_REALM, WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME, WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET, WS_SECURITY_BINDING_PROPERTY_ID, WS_SECURITY_BINDING_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_BINDING_PROPERTY_MESSAGE_PROPERTIES, WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH, WS_SECURITY_BINDING_PROPERTY_REQUIRE_SSL_CLIENT_CERT, WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_SIZE, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_ACTIVE_CONTEXTS, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_PENDING_CONTEXTS, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_RENEWAL_INTERVAL, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_ROLLOVER_INTERVAL, WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_SUPPORT_RENEW, WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE, webservices/WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL, webservices/WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS, webservices/WS_SECURITY_BINDING_PROPERTY_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT, webservices/WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE, webservices/WS_SECURITY_BINDING_PROPERTY_DISABLE_CERT_REVOCATION_CHECK, webservices/WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_BASIC_REALM, webservices/WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_DOMAIN, webservices/WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_REALM, webservices/WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME, webservices/WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET, webservices/WS_SECURITY_BINDING_PROPERTY_ID, webservices/WS_SECURITY_BINDING_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH, webservices/WS_SECURITY_BINDING_PROPERTY_REQUIRE_SSL_CLIENT_CERT, webservices/WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_SIZE, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_ACTIVE_CONTEXTS, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_PENDING_CONTEXTS, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_RENEWAL_INTERVAL, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_ROLLOVER_INTERVAL, webservices/WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_SUPPORT_RENEW, webservices/WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE, wsw.ws_security_binding_property_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_BINDING_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_BINDING_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_BINDING_PROPERTY_ID enumeration


## -description



              Identifies the properties used to specify security
              binding settings.  Security binding settings are present 
              in <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">security bindings</a>
that are used, in turn, in a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a>.
            

This enumeration is used within the <a href="https://msdn.microsoft.com/f2790fd7-6f51-45a5-b2b6-e5aaaaca9660">WS_SECURITY_BINDING_PROPERTY</a> structure, which in turn is used in a <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a> structure. Not all values are applicable to all security bindings. Please see the individual descriptions for a list of security bindings that support the respective property.


Note that the related enum <a href="https://msdn.microsoft.com/d5ba0170-2345-4144-9a60-25c0e638a283">WS_SECURITY_TOKEN_PROPERTY_ID</a>
defines the keys for extracting fields from a security token instance.
Thus, <a href="https://msdn.microsoft.com/f2790fd7-6f51-45a5-b2b6-e5aaaaca9660">WS_SECURITY_BINDING_PROPERTY</a> enables specifying security binding
settings at channel / listener creation time to influence how a
security token is created and used, whereas <b>WS_SECURITY_TOKEN_PROPERTY_ID</b>
enables extracting fields out of a security token -- typically a
security token from a received message when the channel and security
are 'live'.
            


## -enum-fields




### -field WS_SECURITY_BINDING_PROPERTY_REQUIRE_SSL_CLIENT_CERT


A <b>BOOL</b> that specifies whether a client certificate should be demanded when using SSL.  The
default is <b>FALSE</b>.
                


This setting may be specified in the security binding properties of a
server-side <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE


A <a href="https://msdn.microsoft.com/7aa0bbf3-afc0-4deb-9cb3-62e297dd8702">WS_WINDOWS_INTEGRATED_AUTH_PACKAGE</a> value that specifies the specific SSP package (among Kerberos, NTLM, SPNEGO) to be used
when performing Windows Integrated Authentication.  The default is <b>WS_WINDOWS_INTEGRATED_AUTH_PACKAGE_SPNEGO</b>.
                


This setting may be specified in the security binding properties of <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH


A <b>BOOL</b> that specifies whether server authentication is mandatory.  Currently, this setting
is applicable only when using Windows Integrated Authentication based
security.  Setting this to <b>FALSE</b> is strongly
discouraged since, without server authentication, a malicious party
masquerading as the server cannot be detected.
                

The default is <b>TRUE</b> when used with <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and <b>FALSE</b> when used with <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>



If a protocol that does not do server authentication (such as NTLM) is
to be allowed, this property must be set to 
<b>FALSE</b>.


This setting may be specified only in the security binding properties
of a client-side <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and  <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS

A <b>BOOL</b> that specifies 
whether the server should allow clients authenticated anonymously
using Windows Integrated Authentication based security.  The default
is <b>FALSE</b>.
                


This setting may be specified only in the security binding properties
of a server-side <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and  <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL


A <a href="http://go.microsoft.com/fwlink/p/?linkid=182190">SECURITY_IMPERSONATION_LEVEL</a> value that specifies the impersonation level the client wants to allow when using Windows
Integrated Authentication to communicate with a service.  The default impersonation level is <b>SecurityIdentification</b>.
                


This setting may be specified in the security binding properties
of <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>,   <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>, and <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME

                    A <b>ULONG</b> that specifies the HTTP header authentication mode to use. The value specified must be a combination of one or more of
                    <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NONE</a>, <b>WS_HTTP_HEADER_AUTH_SCHEME_BASIC</b>,
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_DIGEST</b>, <b>WS_HTTP_HEADER_AUTH_SCHEME_NTLM</b> or
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</b>. When setting this property on a binding used to communicate
                    with an HTTP proxy server, only one scheme should be set, and <b>WS_HTTP_HEADER_AUTH_SCHEME_NONE</b> 
                    may not be used.



                    Alternatively, this property may be set set to <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</a>.
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</b> must not be combined with any other value and cannot be used to 
                    authenticate to an HTTP proxy server.                    
                


<a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NONE</a> is only supported on the client. Setting it by itself disables HTTP header authentication.
                    Setting it in conjunction with other schemes allows the client to fall back to no header authentication when the server does not require it.
                    Otherwise, if the client specifies multiple authentication schemes and the server requires no authentication the request will fail.
                


                    When setting a single authentication scheme, the client will perform the request with that scheme set. If multiple schemes are set,
                    the client will first probe the server for the supported schemes by sending an unauthenticated blank request. Should the client 
                    and server share more than one supported scheme, the client will prioritize schemes in the following order and pick the first mutually 
                    supported one:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NTLM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_DIGEST</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_BASIC</a>
</li>
</ul>



                    When the scheme is set to <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</a> and Kerberos authentication is negotiated, the Server Principal Name (SPN) 
                    used is derived from the server's DNS name. Even when present <a href="https://msdn.microsoft.com/59c851b4-6e1a-4144-9742-48d5c094d592">WS_ENDPOINT_IDENTITY</a> is ignored. In order for authentication
                    to succeed, the server must be able to decrypt Kerberos tickets for that SPN.
                

When the scheme is set to <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_DIGEST</a> or <b>WS_HTTP_HEADER_AUTH_SCHEME_BASIC</b>, then the <a href="https://msdn.microsoft.com/31a9c242-b56c-47d5-8b5a-a7a245575124">WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> must be used as credential type.


                    Note: Using "localhost", "127.0.0.1" or similar ways to refer to the local machine as server address may cause failures when using 
                    <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NTLM</a> or <b>WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</b>. It is recommended to use the machine name instead.
                


                    This setting may be specified in the security binding properties of <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>. 
                    The default is <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET

A <a href="https://msdn.microsoft.com/d8e9b1b9-70b7-41b3-bbf0-7cd04ebabf55">WS_HTTP_HEADER_AUTH_TARGET</a> value that specifies the HTTP header authentication target to use. This property can be specified 
on the client side to indicate whether the http header authentication security binding 
is for the target server or the proxy server. Default value is <b>WS_HTTP_HEADER_AUTH_TARGET_SERVICE</b>.
                


This setting may be specified in the security binding properties of <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_BASIC_REALM

A <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> s used as the realm with the basic HTTP header
authentication scheme.
                


This setting may be specified in the security binding properties of a
server side <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_REALM


A <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> used as the realm with the digest HTTP
header authentication scheme.
                


This setting may be specified in the security binding properties of a
server side <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_DOMAIN

A <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> used as the domain name with the digest
HTTP header authentication scheme.
                


This setting may be specified in the security binding properties of a
server side <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_SIZE

A <b>ULONG</b> that specifies the key size (in bits) of the security token to be requested from an
issuer.  If unspecified, the issuer decides the size. May be used with the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE


A <a href="https://msdn.microsoft.com/dd6bca9a-e47b-46b3-b9ac-23aecb101337">WS_SECURITY_KEY_ENTROPY_MODE</a> value that specifies how entropy contributes to the key in issued symmetric key
tokens.  The default is <b>WS_SECURITY_KEY_ENTROPY_MODE_COMBINED</b>. 
This setting may be specified in the security binding properties of the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
                


### -field WS_SECURITY_BINDING_PROPERTY_MESSAGE_PROPERTIES


            The set of <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a> to be specified
            while <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">creating the two messages</a> to
            be used for the security token obtaining exchange.  If this property
            is not specified, the request and reply messages are created with the
            default message properties. This setting may be specified in the security binding properties of the  <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_PENDING_CONTEXTS


                  A <b>ULONG</b> that specifies the maximum number of pending security contexts on the service that
                  have not been accepted by the application (or service model) as
                  channels. The default is 100. The setting may be specified in the security binding properties of the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
                


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_MAX_ACTIVE_CONTEXTS


            A <b>ULONG</b> that specifies the maximum number of active security contexts on the service. The default is 1000. 
            The setting may be specified in the security binding properties of  the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION

A <a href="https://msdn.microsoft.com/17c21a3a-1cb5-4174-8300-a5c3d87e3e0f">WS_SECURE_CONVERSATION_VERSION</a> value that specifies the version of WS-SecureConversation to use. The default is <b>WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</b>.
            This setting may be specified in the security binding properties of the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_SUPPORT_RENEW

A <b>BOOL</b> that specifies
            whether or not to support the renew operation on established security contexts. On the client, if this is 
            set to <b>FALSE</b>, instead of renewing the existing security context a new context 
            will be established. On the server, all incoming renew messages will be 
            rejected. The default is <b>TRUE</b>.
            This setting may be specified in the security binding properties of the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_RENEWAL_INTERVAL


            A 	<a href="https://msdn.microsoft.com/f8a42739-e395-4b20-bf3a-3d7c5e3a5495">WS_TIMESPAN</a> structure that contains the interval before which a security context must be renewed. On the client it defaults to 10 hours
            and denotes the time after which the session is proactively renewed. On the server it defaults to 15 hours
            and denotes context lifetime. A server context must be renewed before that limit is reached.
            This setting may be specified in the security binding properties of the 
<a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_ROLLOVER_INTERVAL


            A <a href="https://msdn.microsoft.com/f8a42739-e395-4b20-bf3a-3d7c5e3a5495">WS_TIMESPAN</a> structure that contains the time interval for which an old security context token should be accepted after a renewal. The default is 5 minutes.
            This tolerance interval is provided to smoothly handle application messages during session renewal.
            This setting may be specified in the security binding properties of the 
 <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a> structure.
          


### -field WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE


                    A <b>ULONG</b> that specifies a set of certificate verification failures that are ignored by the client so that communication with 
                    the remote endpoint will succeed regardless. 
                    Any combination of the values defined in <a href="https://msdn.microsoft.com/e2324688-abf5-4b09-b236-502af8e1fcd1">WS_CERT_FAILURE</a> or 0 may be specified. The default is <b>WS_CERT_FAILURE_REVOCATION_OFFLINE</b>.
                    This setting may be specified in the security binding properties of the 
 <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> structure on the client.
                


                    Ignoring certificate verification failures can expose the application to potential security vulnerabilities. 
                    The use of this property should be carefully evaluated.
                


### -field WS_SECURITY_BINDING_PROPERTY_DISABLE_CERT_REVOCATION_CHECK


                    A <b>BOOL</b> that specifies the state of certificate revocation checking.  When set to <b>TRUE</b>, certificate revocation checking is disabled. The default is <b>FALSE</b>. 
                    This setting may be specified in the security binding properties of the 
 <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> structure on the client.
                


                    Disabling certificate revocation checking can expose the application to potential security vulnerabilities. 
                    The use of this property should be carefully evaluated.
                


### -field WS_SECURITY_BINDING_PROPERTY_DISALLOWED_SECURE_PROTOCOLS


### -field WS_SECURITY_BINDING_PROPERTY_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT

A <a href="https://msdn.microsoft.com/1D33A816-2580-4295-994D-6C6DFFBA7A0B">WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</a> structure that specifies a callback which will be invoked for each send request operation. This allows an application to validate the certificate associated with the connection of a request.

