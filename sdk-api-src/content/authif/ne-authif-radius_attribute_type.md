---
UID: NE:authif._RADIUS_ATTRIBUTE_TYPE
title: RADIUS_ATTRIBUTE_TYPE (authif.h)
author: windows-sdk-content
description: The RADIUS_ATTRIBUTE_TYPE type enumerates the possible types for a RADIUS attribute.
old-location: nps\IAS_radius_attribute_type.htm
tech.root: Nps
ms.assetid: b0b39062-0622-48f8-a06a-232713ec8c3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RADIUS_ATTRIBUTE_TYPE, RADIUS_ATTRIBUTE_TYPE enumeration [Network Policy Server], _ias_radius_attribute_type, authif/RADIUS_ATTRIBUTE_TYPE, authif/ratAcctAuthentic, authif/ratAcctDelayTime, authif/ratAcctInputOctets, authif/ratAcctInputPackets, authif/ratAcctOutputOctets, authif/ratAcctOutputPackets, authif/ratAcctSessionId, authif/ratAcctSessionTime, authif/ratAcctStatusType, authif/ratAcctTerminationCause, authif/ratAuthenticator, authif/ratCHAPChallenge, authif/ratCHAPPassword, authif/ratCRPPolicyName, authif/ratCallbackId, authif/ratCallbackNumber, authif/ratCalledStationId, authif/ratCallingStationId, authif/ratClass, authif/ratClearTextPassword, authif/ratCode, authif/ratEAPTLV, authif/ratExtensionState, authif/ratFQUserName, authif/ratFilterId, authif/ratFramedAppleTalkLink, authif/ratFramedAppleTalkNetwork, authif/ratFramedAppleTalkZone, authif/ratFramedCompression, authif/ratFramedIPAddress, authif/ratFramedIPNetmask, authif/ratFramedIPXNetwork, authif/ratFramedIPv6Pool, authif/ratFramedIPv6Prefix, authif/ratFramedIPv6Route, authif/ratFramedInterfaceId, authif/ratFramedMTU, authif/ratFramedProtocol, authif/ratFramedRoute, authif/ratFramedRouting, authif/ratIdentifier, authif/ratIdleTimeout, authif/ratLoginIPHost, authif/ratLoginIPv6Host, authif/ratLoginLATGroup, authif/ratLoginLATNode, authif/ratLoginLATService, authif/ratLoginPort, authif/ratLoginService, authif/ratMediumType, authif/ratMinimum, authif/ratNASIPAddress, authif/ratNASIPv6Address, authif/ratNASIdentifier, authif/ratNASPort, authif/ratNASPortType, authif/ratPolicyName, authif/ratPortLimit, authif/ratProvider, authif/ratProviderName, authif/ratProxyState, authif/ratRejectReasonCode, authif/ratReplyMessage, authif/ratServiceType, authif/ratSessionTimeout, authif/ratSrcIPAddress, authif/ratSrcIPv6Address, authif/ratSrcPort, authif/ratState, authif/ratStrippedUserName, authif/ratTerminationAction, authif/ratTunnelPassword, authif/ratTunnelPrivateGroupID, authif/ratTunnelType, authif/ratUniqueId, authif/ratUserName, authif/ratUserPassword, authif/ratVendorSpecific, ias.radius_attribute_type, nps.IAS_radius_attribute_type, ratAcctAuthentic, ratAcctDelayTime, ratAcctInputOctets, ratAcctInputPackets, ratAcctOutputOctets, ratAcctOutputPackets, ratAcctSessionId, ratAcctSessionTime, ratAcctStatusType, ratAcctTerminationCause, ratAuthenticator, ratCHAPChallenge, ratCHAPPassword, ratCRPPolicyName, ratCallbackId, ratCallbackNumber, ratCalledStationId, ratCallingStationId, ratClass, ratClearTextPassword, ratCode, ratEAPTLV, ratExtensionState, ratFQUserName, ratFilterId, ratFramedAppleTalkLink, ratFramedAppleTalkNetwork, ratFramedAppleTalkZone, ratFramedCompression, ratFramedIPAddress, ratFramedIPNetmask, ratFramedIPXNetwork, ratFramedIPv6Pool, ratFramedIPv6Prefix, ratFramedIPv6Route, ratFramedInterfaceId, ratFramedMTU, ratFramedProtocol, ratFramedRoute, ratFramedRouting, ratIdentifier, ratIdleTimeout, ratLoginIPHost, ratLoginIPv6Host, ratLoginLATGroup, ratLoginLATNode, ratLoginLATService, ratLoginPort, ratLoginService, ratMediumType, ratMinimum, ratNASIPAddress, ratNASIPv6Address, ratNASIdentifier, ratNASPort, ratNASPortType, ratPolicyName, ratPortLimit, ratProvider, ratProviderName, ratProxyState, ratRejectReasonCode, ratReplyMessage, ratServiceType, ratSessionTimeout, ratSrcIPAddress, ratSrcIPv6Address, ratSrcPort, ratState, ratStrippedUserName, ratTerminationAction, ratTunnelPassword, ratTunnelPrivateGroupID, ratTunnelType, ratUniqueId, ratUserName, ratUserPassword, ratVendorSpecific
ms.topic: enum
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - AuthIf.h
api_name:
 - RADIUS_ATTRIBUTE_TYPE
product: Windows
targetos: Windows
req.typenames: RADIUS_ATTRIBUTE_TYPE
req.redist: 
---

# RADIUS_ATTRIBUTE_TYPE enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_ATTRIBUTE_TYPE</b> type enumerates the possible types for a RADIUS attribute.


## -enum-fields




### -field ratMinimum

This value is equal to zero, and used as the null-terminator in any array of 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structures.


### -field ratUserName

Specifies the name of the user to be authenticated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information. Also see 
<a href="https://msdn.microsoft.com/2f741a81-e432-47fe-a14a-8b77ecd41e28">User Identification Attributes</a>.


### -field ratUserPassword

Specifies the password of the user to be authenticated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratCHAPPassword

Specifies the password provided by the user in response to an Challenge Handshake Authentication Protocol (CHAP) challenge. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratNASIPAddress

Specifies the NAS IP address. An Access-Request should specify either an NAS IP address or an NAS identifier. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratNASPort

Identifies the physical or virtual private network (VPN) through which the user is connecting to the NAS. Note that this value is not a port number in the sense of TCP or UDP. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratServiceType

Specifies the type of service the user has requested or the type of service to be provided. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedProtocol

Specifies the type of framed protocol to use for framed access, for example SLIP, PPP, or ARAP (AppleTalk Remote Access Protocol). The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedIPAddress

Specifies the IP address that will be configured for the user requesting authentication. This attribute is typically returned by the authentication provider. However, the NAS may use it in an authentication request to specify a preferred IP address. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedIPNetmask

Specifies the IP network mask for a user that is a router to a network. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedRouting

Specifies the routing method for a user that is a router to a network. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFilterId

Identifies the filter list for the user requesting authentication. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedMTU

Specifies the Maximum Transmission Unit (MTU) for the user. This attribute is used in cases where the MTU is not negotiated through some other means, such as PPP. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedCompression

Specifies a compression protocol to use for the connection. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information


### -field ratLoginIPHost

Specifies the system with which to connect the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratLoginService

Specifies the service to use to connect the user to the host specified by <b>ratLoginIPHost</b>. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratLoginPort

Specifies the port to which to connect the user. This attribute is present only if the <b>ratLoginService</b> attribute is present. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratReplyMessage

Specifies a message to display to the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratCallbackNumber

Specifies a callback number. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratCallbackId

Identifies a location to callback. The value of this attribute is interpreted by the NAS. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedRoute

Provides routing information to configure on the NAS for the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedIPXNetwork

Specifies the IPX network number to configure for the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratState

This attribute is included in Access-Challenge and Access-Accept communications between the server and the client. Please refer to 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for detailed information about this value. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer.


### -field ratClass

Specifies a value that is provided to the NAS by the authentication provider. The NAS should use this value when communicating with the accounting provider. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratVendorSpecific

Allows vendors to provide their own extended attributes. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratSessionTimeout

Specifies the maximum number of seconds for which to provide service to the user. After this time, the session is terminated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratIdleTimeout

Specifies the maximum number of consecutive seconds the session can be idle. If the idle time exceeds this value, the session is terminated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratTerminationAction

Indicates what action the NAS should take when the
      specified service is completed.  It is only used in Access-Accept
      packets. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratCalledStationId

Specifies the number that the user dialed to connect to the NAS. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratCallingStationId

Specifies the number from which the user is calling. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratNASIdentifier

Specifies the NAS identifier. An Access-Request should specify either an NAS identifier or an NAS IP address. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratProxyState

Specifies a value that a proxy server includes when forwarding an authentication request. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratLoginLATService

This attribute is not currently used for authentication on Windows. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratLoginLATNode

This attribute is not currently used for authentication on Windows. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratLoginLATGroup

This attribute is not currently used for authentication on Windows. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedAppleTalkLink

Specifies the AppleTalk network number for a user that is another router. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedAppleTalkNetwork

Specifies the AppleTalk network number that the NAS should use to allocate an AppleTalk node for the user. This attribute is used only when the user is not another router. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratFramedAppleTalkZone

Specifies the AppleTalk default zone for the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratAcctStatusType

Specifies whether the accounting provider should start or stop accounting for the user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctDelayTime

Specifies the length of time that the client has been attempting to send the current request. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctInputOctets

Specifies the number of octets that have been received during the current accounting session. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctOutputOctets

Specifies the number of octets sent during the current accounting session. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctSessionId

Specifies a value to enable the identification of matching start and stop records within a log file. The start and stop records are sent in the <b>ratAcctStatusType</b> attribute. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctAuthentic

Specifies, to the accounting provider, how the user was authenticated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctSessionTime

Specifies the number of seconds that have elapsed in the current accounting session. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctInputPackets

Specifies the number of packets that have been received during the current accounting session. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctOutputPackets

Specifies the number of packets that have been sent during the current accounting session. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratAcctTerminationCause

Specifies how the current accounting session was terminated. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field ratCHAPChallenge

Specifies the CHAP challenge sent by the NAS to a CHAP user. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a pointer. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratNASPortType

Specifies the type of the port through which the user is connecting, for example, asynchronous, ISDN, virtual. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field ratPortLimit

Specifies the number of ports the NAS should make available to the user for multilink sessions. The value field in 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> for this type is a 32-bit integral value. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information


### -field ratTunnelType

Specifies either the tunneling protocol or protocols to be used (in
      the case of a tunnel initiator) or specifies the tunneling protocol in
      use (in the case of a tunnel terminator). See <a href="Http://go.microsoft.com/fwlink/p/?linkid=84058">RFC 2868</a> for more information.


### -field ratMediumType

Specifies the transport medium
      to use when creating a tunnel for protocols, such as L2TP,
      that can operate over multiple transports. See <a href="Http://go.microsoft.com/fwlink/p/?linkid=84058">RFC 2868</a> for more information.


### -field ratTunnelPassword

May contain a password to be used to authenticate
      to a remote server.  It may only be included in an Access-Accept
      packet.


### -field ratTunnelPrivateGroupID

Specifies the group ID for a particular tunneled
      session.


### -field ratNASIPv6Address

Specifies the IPv6 Address of the NAS
      that requests authentication of the user. It should be
      unique to the NAS within the scope of the RADIUS server.  It is only used in an Access-Request packet. See the NAS-IPv6-Address section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratFramedInterfaceId

Specifies the IPv6 interface identifier to be
      configured for the user.  It may be used in an Access-Accept packet.
      See the Framed-Interface-Id section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratFramedIPv6Prefix

Specifies an IPv6 prefix (and corresponding route)
      to be configured for the user.  It may be used in an Access-Accept
      packet and can appear multiple times.  See the Framed-IPv6-Prefix section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratLoginIPv6Host

Specifies the system with which to connect the
      user, when the ratLoginService attribute is included.  It may be
      used in an Access-Accept packet.
See the Login-IPv6-Host section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratFramedIPv6Route

Specifies routing information to be configured for
      the user on the NAS.  It is used in an Access-Accept packet and
      can appear multiple times.
See the Framed-IPv6-Route section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratFramedIPv6Pool

Specifies the name of an assigned pool that should
      be used to assign an IPv6 prefix for the user.  If a NAS does not
      support multiple prefix pools, the NAS must ignore this attribute.

See the Framed-IPv6-Pool section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field ratCode

Specifies the request type code. This is an extended, read-only attribute, used only in the 
<a href="https://msdn.microsoft.com/75af0d43-f866-4769-8221-45e47c588bb0">RadiusExtensionProcess</a> and 
<a href="https://msdn.microsoft.com/7525b719-5741-4256-8759-421a407b9e44">RadiusExtensionProcessEx</a> functions. Its contents can be interpreted by comparing it with <a href="https://msdn.microsoft.com/cb971643-82ca-4302-a961-9d567da04c27">RADIUS_CODE</a> enumeration values.


### -field ratIdentifier

Specifies the request identifier. This is an extended, read-only attribute.


### -field ratAuthenticator

Specifies the request authenticator. This is an extended, read-only attribute.


### -field ratSrcIPAddress

Specifies the source IP address. This is an extended, read-only attribute.


### -field ratSrcPort

Specifies the source IP port. This is an extended, read-only attribute.


### -field ratProvider

Specifies the authentication provider. The value for this attribute is taken from the 
<a href="https://msdn.microsoft.com/017c31f1-1654-4312-a1f0-747ea82391e1">RADIUS_AUTHENTICATION_PROVIDER</a> enumerated type. This is an extended, read-only attribute.


### -field ratStrippedUserName

Specifies the user name with the realm removed. See 
<a href="https://msdn.microsoft.com/2f741a81-e432-47fe-a14a-8b77ecd41e28">User Identification Attributes</a> for more information. This is an extended attribute.


### -field ratFQUserName

Specifies the fully qualified user name. See 
<a href="https://msdn.microsoft.com/2f741a81-e432-47fe-a14a-8b77ecd41e28">User Identification Attributes</a> for more information. This is an extended attribute.


### -field ratPolicyName

Specifies  a remote access  policy name. This is an extended attribute.


### -field ratUniqueId

Specifies a unique ID for the request. This is a read-only attribute.


### -field ratExtensionState

This attribute is used to pass state information between extensions.


### -field ratEAPTLV

Specifies an EAP-TLV packet. For more information about the EAP-TLV packet format, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84020">IETF EAP Working Draft</a>.


### -field ratRejectReasonCode

Specifies the reason code for a RADIUS Reject. For more information, see  <a href="https://msdn.microsoft.com/b8db4404-40ab-4f28-96ce-43359c959546">RADIUS_REJECT_REASON_CODE</a>.


### -field ratCRPPolicyName

Specifies the Connection Request Policy  Name that matched this RADIUS packet.


### -field ratProviderName

Specifies the remote RADIUS server group name for request forwarding.

If the Authentication indicated by <b>ratProvider</b> is a proxy, the extension DLL can change the <b>ratProviderName</b> to indicate which remote server group the request should be forwarded to.


### -field ratClearTextPassword

Specifies the user password in clear text.

To support authorization databases using PEAP-MSChapv2, the extension DLL retrieves the user password from the database and sends it to NPS.


### -field ratSrcIPv6Address

Source IPv6 address. It is not a standard RADIUS attribute. It corresponds to the internal attribute <a href="https://msdn.microsoft.com/42a74deb-6d6e-493a-b9e0-d9549a5530d3">IAS_ATTRIBUTE_CLIENT_IPv6_ADDRESS</a>. This is a read-only attribute.


### -field ratCertificateThumbprint




## -remarks



The following attributes are read-only. Extension DLLs that implement <a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> cannot add/remove/modify these attributes within a request or response contained in a <a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a>.

<ul>
<li><b>ratCode</b></li>
<li><b>ratIdentifier</b></li>
<li><b>ratAuthenticator</b></li>
<li><b>ratSrcIPAddress</b></li>
<li><b>ratSrcPort</b></li>
<li><b>ratProvider</b></li>
<li><b>ratUniqueId</b></li>
<li><b>ratSrcIPv6Address</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/017c31f1-1654-4312-a1f0-747ea82391e1">RADIUS_AUTHENTICATION_PROVIDER</a>
 

 

