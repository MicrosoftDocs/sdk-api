---
UID: NE:webservices.__unnamed_enum_4
title: "__unnamed_enum_4"
author: windows-sdk-content
description: A set of flags used to specify how to match a URL.
old-location: wsw\ws_url_matching_options.htm
tech.root: wsw
ms.assetid: 65449a2d-88c3-431e-83d5-ecb182463cf5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_MATCH_URL_DNS_FULLY_QUALIFIED_HOST, WS_MATCH_URL_DNS_HOST, WS_MATCH_URL_EXACT_PATH, WS_MATCH_URL_HOST_ADDRESSES, WS_MATCH_URL_LOCAL_HOST, WS_MATCH_URL_NETBIOS_HOST, WS_MATCH_URL_NO_QUERY, WS_MATCH_URL_PORT, WS_MATCH_URL_PREFIX_PATH, WS_MATCH_URL_THIS_HOST, WS_URL_MATCHING_OPTIONS, WS_URL_MATCHING_OPTIONS enumeration [Web Services for Windows], __unnamed_enum_4, webservices/WS_MATCH_URL_DNS_FULLY_QUALIFIED_HOST, webservices/WS_MATCH_URL_DNS_HOST, webservices/WS_MATCH_URL_EXACT_PATH, webservices/WS_MATCH_URL_HOST_ADDRESSES, webservices/WS_MATCH_URL_LOCAL_HOST, webservices/WS_MATCH_URL_NETBIOS_HOST, webservices/WS_MATCH_URL_NO_QUERY, webservices/WS_MATCH_URL_PORT, webservices/WS_MATCH_URL_PREFIX_PATH, webservices/WS_MATCH_URL_THIS_HOST, webservices/WS_URL_MATCHING_OPTIONS, wsw.ws_url_matching_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_URL_MATCHING_OPTIONS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_4 enumeration


## -description


A set of flags used to specify how to match a URL.
            


## -enum-fields




### -field WS_MATCH_URL_DNS_HOST

If this flag is specified, and a wildcard (+ or *) was specified
                    used for the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, and the computer
                    is part of a DNS domain, then the host portion of the URL being matched is 
                    compared against the DNS host name of the computer (without the domain portion).
                


### -field WS_MATCH_URL_DNS_FULLY_QUALIFIED_HOST

If this flag is specified, and a wildcard (+ or *) was specified
                    used for the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, and the computer
                    is part of a DNS domain, then the host portion of the URL being matched is
                    compared against the DNS host name of the computer (with the domain portion).
                


### -field WS_MATCH_URL_NETBIOS_HOST

If this flag is specified, and a wildcard (+ or *) was specified
                    used for the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, and the computer
                    has a NETBIOS name, then the host portion of the URL being matched is compared
                    against the NETBIOS name of the computer.
                


### -field WS_MATCH_URL_LOCAL_HOST

If this flag is specified, and a wildcard (+ or *) was specified
                    used for the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, then the host portion of 
                    the URL being matched is compared against the name "localhost".
                


### -field WS_MATCH_URL_HOST_ADDRESSES

If this flag is specified, and a wildcard (+ or *) was specified
                    used for the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> then the host portion of the
                    URL being matched is compared against the adapter addresses of the host machine.
                


### -field WS_MATCH_URL_THIS_HOST

This value is a combination of the following host flags which correspond
                    to different ways of specifying the host name of "this computer".
                

<ul>
<li>WS_MATCH_URL_DNS_HOST
                    </li>
<li>WS_MATCH_URL_DNS_FULLY_QUALIFIED_HOST
                    </li>
<li>WS_MATCH_URL_NETBIOS_HOST
                    </li>
<li>WS_MATCH_URL_LOCAL_HOST
                    </li>
<li>WS_MATCH_URL_HOST_ADDRESSES
                </li>
</ul>

### -field WS_MATCH_URL_PORT

If this flag is set, then the port number in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>is compared against the port number in URL being matched.
                


### -field WS_MATCH_URL_EXACT_PATH

If this flag is set, then the path in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>is compared against the path in URL being matched for an exact match.  This flag may not
                    be specified with <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_PREFIX_PATH</a>.
                


### -field WS_MATCH_URL_PREFIX_PATH

If this flag is set, then the path in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>is compared against the path in the URL being matched for a prefix match ("starts with").
                    This flag may not be specified with <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_EXACT_PATH</a>.
                


### -field WS_MATCH_URL_NO_QUERY

If this flag is set, then the URL being matched only matches if it does not
                    have a query string component.
                


## -remarks



These flags are used to specify the value of the 
                <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a> and
                <b>WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</b> listener properties.
            

When used with <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a>,
                the URL of the <a href="https://msdn.microsoft.com/3207c7f0-7f12-4f6b-8ddd-bac9c06ccfbf">WS_CHANNEL_PROPERTY_TRANSPORT_URL</a> of a SOAP message
                is matched against the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>.
            

When used with <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</a>,
                the URL of the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_TO_HEADER</a> message property of a received 
                message is matched against the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>.
            

The following grammar illustrates the valid combinations of the flags:
            

<pre class="syntax" xml:space="preserve"><code>
Flags := HostFlags PathFlags QueryFlags

HostFlags := 
    WS_MATCH_URL_DNS_HOST?
    WS_MATCH_URL_DNS_FULLY_QUALIFIED_HOST?
    WS_MATCH_URL_NETBIOS_HOST? 
    WS_MATCH_URL_LOCAL_HOST?
    WS_MATCH_URL_PORT?

PathFlags :=
    (WS_MATCH_URL_EXACT_PATH |
    WS_MATCH_URL_PREFIX_PATH | 
    0)?

QueryFlags :=
    WS_MATCH_URL_NO_QUERY?
</code></pre>
The set of flags above control how matching is done for each of the components
                of the URL (host, port, path, query).  If an URL does not match, then then the message 
                will be rejected.  In order for a URL to match, each of the components
                must match.  A component is matched as follows:
            

<ul>
<li>If no flags are specified for a particular component, then
                the component will always match.  This allows an application to enforce
                its own matching logic after receiving the message.
                </li>
<li>If one or more flags are specified for a particular component,
                then the component matches if the logic associated with any of the flags match.
            </li>
</ul>
The host portion of the URL is matched as follows:
            

<ul>
<li>If a host name was specified in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, then that
                host name will be used to match the host portion of the received URL.
                </li>
<li>If a host address was specified in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, then that
                host address will be used to match the host portion of the received URL.
                </li>
<li>If a wildcard (+ or *) was specified in the URL passed to <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a>, then
                the HostFlags (see above grammar) will be used to determine how to match the host portion of the received URL.
            </li>
</ul>


