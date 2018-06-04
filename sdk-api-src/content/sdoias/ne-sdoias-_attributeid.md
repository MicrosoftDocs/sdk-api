---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _ATTRIBUTEID enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008. The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>ATTRIBUTEID</b> enumeration type enumerates the RADIUS attributes supported by the SDO API.


## -enum-fields




### -field ATTRIBUTE_UNDEFINED

Specifies a value equal to zero, and used as the <b>NULL</b> terminator in an array of attributes.


### -field ATTRIBUTE_MIN_VALUE

Specifies the minimum value for values of this enumeration type.


### -field RADIUS_ATTRIBUTE_USER_NAME

Specifies the name of the user to be authenticated. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_USER_PASSWORD

Specifies the password of the user to be authenticated. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_CHAP_PASSWORD

Specifies the password provided by the user in response to an MD5 Challenge Handshake Authentication Protocol (CHAP) challenge. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_NAS_IP_ADDRESS

Specifies the Network Access Server (NAS) IP address. An Access-Request should specify either an NAS IP address or an NAS identifier. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_NAS_PORT

Specifies the physical or virtual private network (VPN) through which the user is connecting to the NAS. Note that this value is not a port number in the sense of TCP or UDP. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_SERVICE_TYPE

Specifies the type of service the user has requested or the type of service to be provided. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_PROTOCOL

Specifies the type of framed protocol to use for framed access, for example SLIP, PPP, or ARAP (AppleTalk Remote Access Protocol). For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IP_ADDRESS

Specifies the IP address that is configured for the user requesting authentication. This attribute is typically returned by the authentication provider. However, the NAS may use it in an authentication request to specify a preferred IP address. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IP_NETMASK

Specifies the IP network mask for a user that is a router to a network. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_ROUTING

Specifies the routing method for a user that is a router to a network. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FILTER_ID

Specifies the filter list for the user requesting authentication. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_MTU

Specifies the Maximum Transmission Unit (MTU) for the user. This attribute is used in cases where the MTU is not negotiated through some other means, such as PPP. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_COMPRESSION

Specifies a compression protocol to use for the connection. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_IP_HOST

Specifies the system with which to connect the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_SERVICE

Specifies the service to use to connect the user to the host specified by <b>raatLoginIPHost</b>. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_TCP_PORT

Specifies the port to which to connect the user. This attribute is present only if the <b>raatLoginService</b> attribute is present. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_UNASSIGNED1

This value is currently unassigned.


### -field RADIUS_ATTRIBUTE_REPLY_MESSAGE

Specifies a message to display to the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_CALLBACK_NUMBER

Specifies a callback number. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_CALLBACK_ID

Specifies a location to call back. The value of this attribute is interpreted by the NAS. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_UNASSIGNED2

This value is currently unassigned. The value field in for this type is also undefined.


### -field RADIUS_ATTRIBUTE_FRAMED_ROUTE

Specifies routing information to configure on the NAS for the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IPX_NETWORK

Specifies the IPX network number to configure for the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_STATE

Specifies state information provided to the client by the server. Refer to 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for detailed information about this value. The value field in for this type is a pointer.


### -field RADIUS_ATTRIBUTE_CLASS

Specifies a value that is provided to the NAS by the authentication provider. The NAS should use this value when communicating with the accounting provider. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_VENDOR_SPECIFIC

Specifies a field for vendor-supplied extended attributes. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_SESSION_TIMEOUT

Specifies the maximum number of seconds for which to provide service to the user. After this time, the session is terminated. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_IDLE_TIMEOUT

Specifies the maximum number of consecutive seconds the session can be idle. If the idle time exceeds this value, the session is terminated. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_TERMINATION_ACTION

Specifies an action the server performs when time the connection terminates. Refer to the above-referenced files for detailed information about this value. The value field in for this type is 32-bit integral value. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_CALLED_STATION_ID

Specifies the number that the user dialed to connect to the NAS. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_CALLING_STATION_ID

Specifies the number from which the user is calling. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_NAS_IDENTIFIER

Specifies the NAS identifier. An Access-Request should specify either an NAS identifier or an NAS IP address. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_PROXY_STATE

Specifies a value that a proxy server includes when forwarding an authentication request. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_LAT_SERVICE

Specifies an attribute that is not currently used for authentication on Windows. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_LAT_NODE

Specifies an attribute that is not currently used for authentication on Windows. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_LAT_GROUP

Specifies an attribute that is not currently used for authentication on Windows. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_APPLETALK_LINK

Specifies the AppleTalk network number for the user when the user is another router. The value field in for this type is 32-bit integral value. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_APPLETALK_NET

Specifies the AppleTalk network number that the NAS should use to allocate an AppleTalk node for the user. This attribute is used only when the user is not another router. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_APPLETALK_ZONE

Specifies the AppleTalk default zone for the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_ACCT_STATUS_TYPE

Specifies whether the accounting provider should start or stop accounting for the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_DELAY_TIME

Specifies the length of time that the client has been attempting to send the current request. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_INPUT_OCTETS

Specifies the number of octets that have been received during the current accounting session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_OUTPUT_OCTETS

Specifies the number of octets that were sent during the current accounting session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_SESSION_ID

Specifies a value to enable the identification of matching start and stop records within a log file. The start and stop records are sent in the <b>raatAcctStatusType</b> attribute. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_AUTHENTIC

Specifies, to the accounting provider, how the user was authenticated; for example by Windows Directory Services, RADIUS, or some other authentication provider. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_SESSION_TIME

Specifies the number of seconds that have elapsed in the current accounting session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_INPUT_PACKETS

Specifies the number of packets that are received during the current accounting session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_OUTPUT_PACKETS

Specifies the number of packets that are sent during the current accounting session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_TERMINATE_CAUSE

Specifies how the current accounting session was terminated. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_MULTI_SSN_ID

Specifies a value to enable the identification of related accounting sessions within a log file. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_ACCT_LINK_COUNT

Specifies the number of links if the current accounting session is using a multilink connection. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_CHAP_CHALLENGE

Specifies the CHAP challenge sent by the NAS to a CHAP user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_NAS_PORT_TYPE

Specifies the type of the port through which the user is connecting, for example, asynchronous, ISDN, virtual. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_PORT_LIMIT

Specifies the number of ports the NAS should make available to the user for multilink sessions. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_LAT_PORT

Specifies an attribute that is not currently used for authentication on Windows. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.


### -field RADIUS_ATTRIBUTE_TUNNEL_TYPE

Specifies the tunneling protocol used. The following list lists valid tunnel types.

<table>
<tr>
<th>Tunnel type value</th>
<th>Description</th>
</tr>
<tr>
<td>1</td>
<td>Point-to-Point Tunneling Protocol (PPTP)</td>
</tr>
<tr>
<td>2</td>
<td>Layer Two Forwarding (L2F)</td>
</tr>
<tr>
<td>3</td>
<td>Layer Two Tunneling Protocol (L2TP)</td>
</tr>
<tr>
<td>4</td>
<td>Ascend Tunnel Management Protocol (ATMP)</td>
</tr>
<tr>
<td>5</td>
<td>Virtual Tunneling Protocol (VTP)</td>
</tr>
<tr>
<td>6</td>
<td>IP Authentication Header in the Tunnel-mode</td>
</tr>
<tr>
<td>7</td>
<td>IP-in-IP Encapsulation (IP-IP)</td>
</tr>
<tr>
<td>8</td>
<td>Minimal IP-in-IP Encapsulation (MIN-IP-IP)</td>
</tr>
<tr>
<td>9</td>
<td>IP Encapsulating Security Payload in the Tunnel-mode (ESP)</td>
</tr>
<tr>
<td>10</td>
<td>Generic Route Encapsulation (GRE)</td>
</tr>
<tr>
<td>11</td>
<td>Bay Dial Virtual Services (DVS)</td>
</tr>
<tr>
<td>12</td>
<td>IP-in-IP Tunneling</td>
</tr>
</table>
 


### -field RADIUS_ATTRIBUTE_TUNNEL_MEDIUM_TYPE

Specifies which transport medium to use when creating a tunnel for those protocols (such as L2TP) that can operate over multiple transports. The following list lists valid medium types.

<table>
<tr>
<th>Medium type value</th>
<th>Description</th>
</tr>
<tr>
<td>1</td>
<td>IPv4 (IP version 4)</td>
</tr>
<tr>
<td>2</td>
<td>IPv6 (IP version 6)</td>
</tr>
<tr>
<td>3</td>
<td>OSI Network Service Access Points (NSAP) Signaling Protocol (see ISO 8348 and ITU-T X.213).</td>
</tr>
<tr>
<td>4</td>
<td>High-Level Data Link Control (HDLC) Protocol (8-bit multidrop)</td>
</tr>
<tr>
<td>5</td>
<td>Bolt Beranek and Newman, Inc. (BBN) Report 1822</td>
</tr>
<tr>
<td>6</td>
<td>IEEE 802 (includes all 802 media plus Ethernet "canonical format")</td>
</tr>
<tr>
<td>7</td>
<td>E.163 Plain Old Telephone Service (POTS)</td>
</tr>
<tr>
<td>8</td>
<td>E.164 Switched Multimegabit Data Service (SMDS), Frame Relay, Asynchronous Transfer Mode (ATM)</td>
</tr>
<tr>
<td>9</td>
<td>F.69 (Telex)</td>
</tr>
<tr>
<td>10</td>
<td>X.121 (X.25, Frame Relay)</td>
</tr>
<tr>
<td>11</td>
<td>Internetwork Packet Exchange (IPX)</td>
</tr>
<tr>
<td>12</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>13</td>
<td>Decnet IV</td>
</tr>
<tr>
<td>14</td>
<td>Banyan Vines</td>
</tr>
<tr>
<td>15</td>
<td>E.164 with NSAP format subaddress</td>
</tr>
</table>
 


### -field RADIUS_ATTRIBUTE_TUNNEL_CLIENT_ENDPT

Specifies the address of the initiator end of the tunnel.


### -field RADIUS_ATTRIBUTE_TUNNEL_SERVER_ENDPT

Specifies the address of the server end of the tunnel.


### -field RADIUS_ATTRIBUTE_ACCT_TUNNEL_CONN

Specifies an identifier assigned to the tunnel
         session. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84057">RFC 2867</a>.


### -field RADIUS_ATTRIBUTE_TUNNEL_PASSWORD

The password for authenticating to the remote server.


### -field RADIUS_ATTRIBUTE_ARAP_PASSWORD

Specifies a password to use for AppleTalk Remote Access Protocol (ARAP) authentication. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_ARAP_FEATURES

Specifies information that an NAS should send back to the user in an ARAP "feature flags" packet. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_ARAP_ZONE_ACCESS

Specifies how to use the ARAP zone list for the user. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_ARAP_SECURITY

Specifies an ARAP security module to use during a secondary authentication phase between the NAS and the user. The value field for this type is a 32-bit integral. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_ARAP_SECURITY_DATA

Specifies the data to use with an ARAP security module. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_PASSWORD_RETRY

Specifies the number of password retry attempts to permit the user access. The value field for this type is a 32-bit integral value.


### -field RADIUS_ATTRIBUTE_PROMPT

Specifies whether the NAS should echo the user response to a challenge. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_CONNECT_INFO

Specifies information about the type of connection the user is using. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_CONFIGURATION_TOKEN

Specifies user-profile information in communications between RADIUS Proxy Servers and RADIUS Proxy Clients. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_EAP_MESSAGE

Specifies that EAP information be sent directly between the user and the authentication provider. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_SIGNATURE

Specifies a signature to include with CHAP, EAP, or ARAP packets. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_TUNNEL_PVT_GROUP_ID

Group ID for a particular tunneled session.


### -field RADIUS_ATTRIBUTE_TUNNEL_ASSIGNMENT_ID

Specifies a tunnel to which a session is assigned.


### -field RADIUS_ATTRIBUTE_TUNNEL_PREFERENCE

Relative preference assigned to each tunnel when more than one set of tunneling attributes is returned to the tunnel initiator.


### -field RADIUS_ATTRIBUTE_ARAP_CHALLENGE_RESPONSE

Specifies the response to a Apple Remote Access Protocol (ARAP) challenge. In ARAP, either the server or the client responds to challenges. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84059">RFC 2869</a>.


### -field RADIUS_ATTRIBUTE_ACCT_INTERIM_INTERVAL

Indicates the number of seconds between each interim update for this specific session. This value can only appear in the Access-Accept message. For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a>.


### -field RADIUS_ATTRIBUTE_NAS_IPv6_ADDRESS

Specifies the IPv6 Address of the NAS that requests authentication of the user. It should be unique to the NAS within the scope of the RADIUS server. It is only used in an Access-Request packet. For more information, see the NAS-IPv6-Address section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_INTERFACE_ID

Specifies the IPv6 interface identifier to be
      configured for the user.  It may be used in an Access-Accept packet.
      For more information, see the Framed-Interface-Id section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IPv6_PREFIX

Specifies an IPv6 prefix (and corresponding route)
      to be configured for the user.  It may be used in an Access-Accept
      packet and can appear multiple times.  For more information, see the Framed-IPv6-Prefix section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field RADIUS_ATTRIBUTE_LOGIN_IPv6_HOST

Specifies the system with which to connect the
      user, when the ratLoginService attribute is included.  It may be
      used in an Access-Accept packet.
For more information, see the Login-IPv6-Host section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IPv6_ROUTE

Specifies routing information to be configured for
      the user on the NAS.  It is used in an Access-Accept packet and
      can appear multiple times.
For more information, see the Framed-IPv6-Route section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field RADIUS_ATTRIBUTE_FRAMED_IPv6_POOL

Specifies the name of an assigned pool that should
      be used to assign an IPv6 prefix for the user.  If a NAS does not
      support multiple prefix pools, the NAS must ignore this attribute.

For more information, see the Framed-IPv6-Pool section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a>.


### -field IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_IP_ADDRESS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_SAVED_RADIUS_CALLBACK_NUMBER

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_NP_CALLING_STATION_ID

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_SAVED_NP_CALLING_STATION_ID

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_ROUTE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_IGNORE_USER_DIALIN_PROPERTIES

Specifies that the user's dial-in properties are ignored.


### -field IAS_ATTRIBUTE_NP_TIME_OF_DAY

Time periods and days of week during which user is allowed to connect.


### -field IAS_ATTRIBUTE_NP_CALLED_STATION_ID

Phone number dialed by user.


### -field IAS_ATTRIBUTE_NP_ALLOWED_PORT_TYPES

Port types permitted for a connection.


### -field IAS_ATTRIBUTE_NP_AUTHENTICATION_TYPE

Authentication types permitted for a connection.


### -field IAS_ATTRIBUTE_NP_ALLOWED_EAP_TYPE

EAP encryption modes permitted for a connection.


### -field IAS_ATTRIBUTE_SHARED_SECRET

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_IP_ADDRESS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_PACKET_HEADER

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_TOKEN_GROUPS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_ALLOW_DIALIN

Specifies whether dial-in access is available for a given user.


### -field IAS_ATTRIBUTE_REQUEST_ID

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_MANIPULATION_TARGET

The target data to which an attribute manipulation rule is applied. Attribute manipulation was previously known as 'realms processing'. See the online help for Internet Authentication Service for more information on attribute manipulation.


### -field IAS_ATTRIBUTE_MANIPULATION_RULE

The manipulation rule to apply to the data specified by the Manipulation-Target attribute. See the online help for Internet Authentication Service for more information on attribute manipulation.


### -field IAS_ATTRIBUTE_ORIGINAL_USER_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_VENDOR_TYPE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_UDP_PORT

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_CHALLENGE

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_RESPONSE

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_DOMAIN

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_ERROR

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_CPW1

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_CPW2

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_LM_ENC_PW

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_NT_ENC_PW

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP_MPPE_KEYS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_AUTHENTICATION_TYPE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_NT4_ACCOUNT_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_FULLY_QUALIFIED_USER_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_NTGROUPS

Specifies groups used for the policy conditions.


### -field IAS_ATTRIBUTE_EAP_FRIENDLY_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_AUTH_PROVIDER_TYPE

The type of authentication provider to use.


### -field MS_ATTRIBUTE_ACCT_AUTH_TYPE

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_ACCT_EAP_TYPE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PACKET_TYPE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_AUTH_PROVIDER_NAME

The name of the RADIUS server or server group that provides authentication.


### -field IAS_ATTRIBUTE_ACCT_PROVIDER_TYPE

The type of accounting provider to use.


### -field IAS_ATTRIBUTE_ACCT_PROVIDER_NAME

The name of the RADIUS server that provides accounting.


### -field MS_ATTRIBUTE_MPPE_SEND_KEY

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_MPPE_RECV_KEY

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_REASON_CODE

Specifies an MS-CHAP reason-for-failure code. This attribute is returned in the Failure packet Message field. For more information, see Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84041">2433</a>.


### -field MS_ATTRIBUTE_FILTER

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field MS_ATTRIBUTE_CHAP2_RESPONSE

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP2_SUCCESS

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_CHAP2_CPW

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_RAS_VENDOR

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field MS_ATTRIBUTE_RAS_VERSION

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field IAS_ATTRIBUTE_NP_NAME

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_PRIMARY_DNS_SERVER

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field MS_ATTRIBUTE_SECONDARY_DNS_SERVER

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field MS_ATTRIBUTE_PRIMARY_NBNS_SERVER

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field MS_ATTRIBUTE_SECONDARY_NBNS_SERVER

See Request for Comments (RFC) 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">2548</a>, Microsoft Vendor-specific RADIUS Attributes.


### -field IAS_ATTRIBUTE_PROXY_POLICY_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PROVIDER_TYPE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PROVIDER_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_REMOTE_SERVER_ADDRESS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_GENERATE_CLASS_ATTRIBUTE

Specifies whether NPS automatically generates the class attribute. NPS automatically generates the class attribute by default.


### -field MS_ATTRIBUTE_RAS_CLIENT_NAME

Specifies the name of the client generating a request.


### -field MS_ATTRIBUTE_RAS_CLIENT_VERSION

Specifies the version of the client generating a request.


### -field IAS_ATTRIBUTE_ALLOWED_CERTIFICATE_EKU

Specifies the certificate purpose or usage object identifiers (OIDs), in dotted decimal notation, that are allowed  when performing certificate-based authentication with EAP-TLS.


### -field IAS_ATTRIBUTE_EXTENSION_STATE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_GENERATE_SESSION_TIMEOUT

Specifies whether NPS automatically generates the session timeout based on user account expiration and time-of-day restrictions. NPS does not automatically generate the session timeout by default.


### -field IAS_ATTRIBUTE_SESSION_TIMEOUT

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_QUARANTINE_IPFILTER

Specifies the IP traffic filter used by the Routing and Remote Access service when the connection is in a restricted state.


### -field MS_ATTRIBUTE_QUARANTINE_SESSION_TIMEOUT

Specifies the time (in seconds) that the connection can remain in a restricted state before being disconnected.


### -field MS_ATTRIBUTE_USER_SECURITY_IDENTITY

Specifies the SID of the user requesting access.


### -field IAS_ATTRIBUTE_REMOTE_RADIUS_TO_WINDOWS_USER_MAPPING

Specifies that Windows authorization is enabled for users authenticated by the remote RADIUS server for example, allows  use with Passport user mapping.


### -field IAS_ATTRIBUTE_PASSPORT_USER_MAPPING_UPN_SUFFIX

Specifies the UPN suffix of the Passport to Windows user mapping.


### -field IAS_ATTRIBUTE_TUNNEL_TAG

Used to set the tag byte for any tunnel attributes in the profile. If this is not set, the default is zero.


### -field IAS_ATTRIBUTE_NP_PEAPUPFRONT_ENABLED

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CERTIFICATE_EKU

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_EAP_CONFIG

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PEAP_EMBEDDED_EAP_TYPEID

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PEAP_FAST_ROAMED_SESSION

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_EAP_TYPEID

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_EAP_TLV

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_REJECT_REASON_CODE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PROXY_EAP_CONFIG

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_EAP_SESSION

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_IS_REPLAY

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLEAR_TEXT_PASSWORD

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_IDENTITY_TYPE

Specifies the type of identity check to perform.


### -field MS_ATTRIBUTE_SERVICE_CLASS

Specifies which group of DHCP scopes correspond to the client requesting access.


### -field MS_ATTRIBUTE_QUARANTINE_USER_CLASS

Vendor-specific attribute used to carry the name of a special DHCP user class, as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3004</a>, called Network Access Protection (NAP) user class.


### -field MS_ATTRIBUTE_QUARANTINE_STATE

Specifies the target quarantine state of the client.


### -field IAS_ATTRIBUTE_OVERRIDE_RAP_AUTH

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_PEAP_CHANNEL_UP

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_NAME_MAPPED

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_POLICY_ENFORCED

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_MACHINE_NTGROUPS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_USER_NTGROUPS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_MACHINE_TOKEN_GROUPS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_USER_TOKEN_GROUPS

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_QUARANTINE_GRACE_TIME

Specifies the amount of time a host has to become conformant with network policy.


### -field IAS_ATTRIBUTE_QUARANTINE_URL

This attribute is reserved for system 
use.


### -field IAS_ATTRIBUTE_QUARANTINE_FIXUP_SERVERS

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_NOT_QUARANTINE_CAPABLE

Vendor-specific attribute that specifies if the client is capable of reporting its state to the network access server (NAS). It must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td> The client sent a Statement of Health (SoH).</td>
</tr>
<tr>
<td>1</td>
<td> The client did not send an SoH.</td>
</tr>
</table>
 


### -field IAS_ATTRIBUTE_QUARANTINE_SYSTEM_HEALTH_RESULT

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_QUARANTINE_SYSTEM_HEALTH_VALIDATORS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_MACHINE_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_NT4_MACHINE_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_QUARANTINE_SESSION_HANDLE

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_FULLY_QUALIFIED_MACHINE_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_QUARANTINE_FIXUP_SERVERS_CONFIGURATION

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_CLIENT_QUARANTINE_COMPATIBLE

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_NETWORK_ACCESS_SERVER_TYPE

Specifies the access type of a network access server (NAS). A NAS may send this attribute to a RADIUS server to indicate the type of this NAS in an Access-Request message.


### -field IAS_ATTRIBUTE_QUARANTINE_SESSION_ID

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_AFW_QUARANTINE_ZONE

Vendor-specific attribute used as a hint for dynamic selection of a preconfigured Internet Protocol security (IPsec) policy by the client requesting access.


### -field MS_ATTRIBUTE_AFW_PROTECTION_LEVEL

Vendor-specific attribute used as a hint for dynamic selection of a preconfigured IPsec policy by the client requesting access.


### -field IAS_ATTRIBUTE_QUARANTINE_UPDATE_NON_COMPLIANT

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_REQUEST_START_TIME

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_MACHINE_NAME

Vendor-specific attribute used to communicate the machine name of the client requesting network access.


### -field IAS_ATTRIBUTE_CLIENT_IPv6_ADDRESS

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_INTERFACE_ID

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_IPv6_PREFIX


### -field IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_IPv6_ROUTE


### -field MS_ATTRIBUTE_QUARANTINE_GRACE_TIME_CONFIGURATION


### -field MS_ATTRIBUTE_IPv6_FILTER

Vendor-specific attribute used to limit the inbound and/or outbound access of the endpoint client.


### -field MS_ATTRIBUTE_IPV4_REMEDIATION_SERVERS

Specifies a list of servers that should be reachable by a quarantined client so that it may remediate itself.


### -field MS_ATTRIBUTE_IPV6_REMEDIATION_SERVERS

Specifies a list of servers that should be reachable by a quarantined client so that it may remediate itself.


### -field IAS_ATTRIBUTE_PROXY_RETRY_COUNT

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_MACHINE_INVENTORY

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_ABSOLUTE_TIME

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_QUARANTINE_SOH

Vendor-specific attribute used only to carry Statement of Health (SoH) information when EAP is not used. A RADIUS server may send it to an network access server (NAS) in an Access-Accept message.


### -field IAS_ATTRIBUTE_EAP_TYPES_CONFIGURED_IN_PROXYPOLICY

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_HCAP_LOCATION_GROUP_NAME

Vendor-specific attribute specifying the location group name for the HCAP entity.


### -field MS_ATTRIBUTE_EXTENDED_QUARANTINE_STATE

Specifies the additional Quarantine state information for a user requesting access to this NAS.


### -field IAS_ATTRIBUTE_SOH_CARRIER_EAPTLV

This attribute is reserved for system use.


### -field MS_ATTRIBUTE_HCAP_USER_GROUPS

An NAS may use this attribute to pass the group name of the user requesting network access to a RADIUS server, which may then use this information to make authentication or authorization decisions.


### -field IAS_ATTRIBUTE_SAVED_MACHINE_HEALTHCHECK_ONLY

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_POLICY_EVALUATED_SHV

Multiple instances of this attribute 
can be present at one time.


### -field MS_ATTRIBUTE_RAS_CORRELATION_ID

TBD


### -field MS_ATTRIBUTE_HCAP_USER_NAME

An NAS may use this attribute to pass the name of the user requesting network access to a RADIUS server, which may then use this information to make authentication or authorization decisions.


### -field IAS_ATTRIBUTE_NT4_HCAP_ACCOUNT_NAME

This attribute is reserved for system use.


### -field IAS_ATTRIBUTE_USER_TOKEN_SID

SID for IAS_ATTRIBUTE_NT4_ACCOUNT_NAME or IAS_ATTRIBUTE_NT4_HCAP_ACCOUNT_NAME 
      regardless of whether the later is a user account or a machine account.


### -field IAS_ATTRIBUTE_MACHINE_TOKEN_SID

SID for IAS_ATTRIBUTE_NT4_MACHINE_NAME.


### -field IAS_ATTRIBUTE_MACHINE_VALIDATED

TBD


### -field MS_ATTRIBUTE_USER_IPv4_ADDRESS

Specifies the IPv4 address of the user.


### -field MS_ATTRIBUTE_USER_IPv6_ADDRESS

Specifies the IPv4 address of the user.


### -field MS_ATTRIBUTE_TSG_DEVICE_REDIRECTION

Vendor-specific attribute for TS Gateway Device Redirection flags.


### -field IAS_ATTRIBUTE_ACCEPT_REASON_CODE

TBD


### -field IAS_ATTRIBUTE_LOGGING_RESULT

TBD


### -field IAS_ATTRIBUTE_SERVER_IP_ADDRESS

TBD


### -field IAS_ATTRIBUTE_SERVER_IPv6_ADDRESS

TBD


### -field IAS_ATTRIBUTE_RADIUS_USERNAME_ENCODING_ASCII

TBD


### -field MS_ATTRIBUTE_RAS_ROUTING_DOMAIN_ID


### -field IAS_ATTRIBUTE_CERTIFICATE_THUMBPRINT


### -field RAS_ATTRIBUTE_ENCRYPTION_TYPE

Specifies the encryption type of the user's connection.


### -field RAS_ATTRIBUTE_ENCRYPTION_POLICY

Specifies the whether encryption is Allowed, Required, or None (disallowed). For more information, see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">RFC 2548</a>.


### -field RAS_ATTRIBUTE_BAP_REQUIRED

Specifies whether bandwidth allocation protocol (BAP) is required.


### -field RAS_ATTRIBUTE_BAP_LINE_DOWN_TIME

Time in seconds for the capacity utilization calculation.


### -field RAS_ATTRIBUTE_BAP_LINE_DOWN_LIMIT

Percent of capacity utilized at which to bring a line down for this user.


#### - IAS_ATTRIBUTE_NP_CONSTRAINT

This attribute is reserved for system use.


#### - IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_IPV6_PREFIX

This attribute is reserved for system use.


#### - IAS_ATTRIBUTE_SAVED_RADIUS_FRAMED_IPV6_ROUTE

This attribute is reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/af7d220d-f920-4480-9cf1-72a2cb542e4e">Attributes</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>
 

 

