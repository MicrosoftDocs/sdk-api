---
UID: NS:mprapi._MPR_INTERFACE_3
title: MPR_INTERFACE_3 (mprapi.h)
description: Contains data for a router demand-dial interface. (MPR_INTERFACE_3)
helpviewer_keywords: ["*PMPR_INTERFACE_3","MPRDM_DialAll","MPRDM_DialAsNeeded","MPRDT_Atm","MPRDT_FrameRelay","MPRDT_Generic","MPRDT_Irda","MPRDT_Isdn","MPRDT_Modem","MPRDT_Pad","MPRDT_Parallel","MPRDT_SW56","MPRDT_Serial","MPRDT_Sonet","MPRDT_Vpn","MPRDT_X25","MPRET_Direct","MPRET_Phone","MPRET_Vpn","MPRIDS_Disabled","MPRIDS_UseGlobalValue","MPRIO_DisableLcpExtensions","MPRIO_IpHeaderCompression","MPRIO_NetworkLogon","MPRIO_PromoteAlternates","MPRIO_RemoteDefaultGateway","MPRIO_RequireCHAP","MPRIO_RequireDataEncryption","MPRIO_RequireEAP","MPRIO_RequireEncryptedPw","MPRIO_RequireMsCHAP","MPRIO_RequireMsCHAP2","MPRIO_RequireMsEncryptedPw","MPRIO_RequirePAP","MPRIO_RequireSPAP","MPRIO_SecureLocalFiles","MPRIO_SharedPhoneNumbers","MPRIO_SpecificIpAddr","MPRIO_SpecificNameServers","MPRIO_SwCompression","MPRIO_UseLogonCredentials","MPRNP_Ip","MPRNP_Ipx","MPR_ET_None","MPR_ET_Optional","MPR_ET_Require","MPR_ET_RequireMax","MPR_INTERFACE_3","MPR_INTERFACE_3 structure [RAS]","MPR_VS_Default","MPR_VS_L2tpFirst","MPR_VS_L2tpOnly","MPR_VS_PptpFirst","MPR_VS_PptpOnly","PMPR_INTERFACE_3","PMPR_INTERFACE_3 structure pointer [RAS]","mprapi/MPR_INTERFACE_3","mprapi/PMPR_INTERFACE_3","rras.mpr_interface_3"]
old-location: rras\mpr_interface_3.htm
tech.root: RRAS
ms.assetid: d761a9cf-7b56-48ad-b98b-60fc99d0d8ba
ms.date: 12/05/2018
ms.keywords: '*PMPR_INTERFACE_3, MPRDM_DialAll, MPRDM_DialAsNeeded, MPRDT_Atm, MPRDT_FrameRelay, MPRDT_Generic, MPRDT_Irda, MPRDT_Isdn, MPRDT_Modem, MPRDT_Pad, MPRDT_Parallel, MPRDT_SW56, MPRDT_Serial, MPRDT_Sonet, MPRDT_Vpn, MPRDT_X25, MPRET_Direct, MPRET_Phone, MPRET_Vpn, MPRIDS_Disabled, MPRIDS_UseGlobalValue, MPRIO_DisableLcpExtensions, MPRIO_IpHeaderCompression, MPRIO_NetworkLogon, MPRIO_PromoteAlternates, MPRIO_RemoteDefaultGateway, MPRIO_RequireCHAP, MPRIO_RequireDataEncryption, MPRIO_RequireEAP, MPRIO_RequireEncryptedPw, MPRIO_RequireMsCHAP, MPRIO_RequireMsCHAP2, MPRIO_RequireMsEncryptedPw, MPRIO_RequirePAP, MPRIO_RequireSPAP, MPRIO_SecureLocalFiles, MPRIO_SharedPhoneNumbers, MPRIO_SpecificIpAddr, MPRIO_SpecificNameServers, MPRIO_SwCompression, MPRIO_UseLogonCredentials, MPRNP_Ip, MPRNP_Ipx, MPR_ET_None, MPR_ET_Optional, MPR_ET_Require, MPR_ET_RequireMax, MPR_INTERFACE_3, MPR_INTERFACE_3 structure [RAS], MPR_VS_Default, MPR_VS_L2tpFirst, MPR_VS_L2tpOnly, MPR_VS_PptpFirst, MPR_VS_PptpOnly, PMPR_INTERFACE_3, PMPR_INTERFACE_3 structure pointer [RAS], mprapi/MPR_INTERFACE_3, mprapi/PMPR_INTERFACE_3, rras.mpr_interface_3'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MPR_INTERFACE_3, *PMPR_INTERFACE_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_INTERFACE_3
 - mprapi/_MPR_INTERFACE_3
 - PMPR_INTERFACE_3
 - mprapi/PMPR_INTERFACE_3
 - MPR_INTERFACE_3
 - mprapi/MPR_INTERFACE_3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_INTERFACE_3
---

# MPR_INTERFACE_3 structure


## -description

The 
<b>MPR_INTERFACE_3</b> structure contains data for a router demand-dial interface.

## -struct-fields

### -field wszInterfaceName

A pointer to a Unicode string that contains the name of the interface.

### -field hInterface

A handle to the interface.

### -field fEnabled

A value that specifies whether the interface is enabled. This value is <b>TRUE</b> if the interface is enabled, <b>FALSE</b> if the interface is administratively disabled.

### -field dwIfType

A value that identifies the 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_interface_type">interface type</a>.

### -field dwConnectionState

A value that describes the current state of the interface, for example, connected, disconnected, or unreachable. For more information and a list of possible states, see 
<a href="/windows/desktop/api/mprapi/ne-mprapi-router_connection_state">ROUTER_CONNECTION_STATE</a>.

### -field fUnReachabilityReasons

A value that describes the reason why  the interface is unreachable. For more information and a list of possible values, see <a href="/windows/desktop/RRAS/unreachability-reasons">Unreachability Reasons</a>.

### -field dwLastError

A value that contains a nonzero value if the interface fails to connect.

### -field dwfOptions

A value that specifies bit flags that are used to set connection options. You can set one of the flags listed in the following table.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRIO_SpecificIpAddr"></a><a id="mprio_specificipaddr"></a><a id="MPRIO_SPECIFICIPADDR"></a><dl>
<dt><b>MPRIO_SpecificIpAddr</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS attempts to use the IP address specified by <b>ipaddr</b> as the IP address for the dial-up connection. If this flag is not set, the value of the <b>ipaddr</b> member is ignored.

Setting the <b>MPRIO_SpecificIpAddr</b> flag corresponds to selecting the <b>Specify an IP Address</b> setting in the TCP/IP settings dialog box. Clearing the <b>MPRIO_SpecificIpAddr</b> flag corresponds to selecting the <b>Server Assigned IP Address</b> setting in the <b>TCP/IP Settings</b> dialog box.

Currently, an IP address set in the phone-book entry properties or retrieved from a server overrides the IP address set in the network control panel.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_SpecificNameServers"></a><a id="mprio_specificnameservers"></a><a id="MPRIO_SPECIFICNAMESERVERS"></a><dl>
<dt><b>MPRIO_SpecificNameServers</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS uses the <b>ipaddrDns</b>, <b>ipaddrDnsAlt</b>, <b>ipaddrWins</b>, and <b>ipaddrWinsAlt</b> members to specify the name server addresses for the dial-up connection. If this flag is not set, RRAS ignores these members.

Setting the MPRIO_SpecificNameServers flag corresponds to selecting the <b>Specify Name Server Addresses</b> setting in the TCP/IP Settings dialog box. Clearing the <b>MPRIO_SpecificNameServers</b> flag corresponds to selecting the <b>Server Assigned Name Server Addresses</b> setting in the <b>TCP/IP Settings</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_IpHeaderCompression"></a><a id="mprio_ipheadercompression"></a><a id="MPRIO_IPHEADERCOMPRESSION"></a><dl>
<dt><b>MPRIO_IpHeaderCompression</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS negotiates to use IP header compression on PPP connections. IP header compression can significantly improve performance.

If this flag is not set, IP header compression is not negotiated.

This flag corresponds to the <b>Use IP Header Compression</b> check box in the <b>TCP/IP Settings</b> dialog box. The flag should be cleared only when connecting to a server that does not correctly negotiate IP header compression.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RemoteDefaultGateway"></a><a id="mprio_remotedefaultgateway"></a><a id="MPRIO_REMOTEDEFAULTGATEWAY"></a><dl>
<dt><b>MPRIO_RemoteDefaultGateway</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the default route for IP packets is through the dial-up adapter when the connection is active. If this flag is cleared, the default route is not modified.

This flag corresponds to the <b>Use Default Gateway on Remote Network</b> check box in the <b>TCP/IP Settings</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_DisableLcpExtensions"></a><a id="mprio_disablelcpextensions"></a><a id="MPRIO_DISABLELCPEXTENSIONS"></a><dl>
<dt><b>MPRIO_DisableLcpExtensions</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS disables the PPP LCP extensions defined in <a href="/windows/desktop/RRAS/routing-request-for-comments">RFC 1570</a>. Disabling the PPP LCP extensions may be necessary to connect to certain older PPP implementations, but it interferes with features such as server callback. Do not set this flag unless it is specifically required.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_SwCompression"></a><a id="mprio_swcompression"></a><a id="MPRIO_SWCOMPRESSION"></a><dl>
<dt><b>MPRIO_SwCompression</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, software compression is negotiated on the link. Setting this flag causes the PPP driver to attempt to negotiate Compression Control Protocol (CCP) with the server. This flag should be set by default, but clearing it can reduce the negotiation period if the server does not support a compatible compression protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireEncryptedPw"></a><a id="mprio_requireencryptedpw"></a><a id="MPRIO_REQUIREENCRYPTEDPW"></a><dl>
<dt><b>MPRIO_RequireEncryptedPw</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, only secure password schemes can be used to authenticate the client with the server. This prevents the PPP driver from using the PAP plain-text authentication protocol to authenticate the client. However, the MS-CHAP, MD5-CHAP, and SPAP authentication protocols are supported. For increased security, set this flag. For increased interoperability, clear this flag. 

This flag corresponds to the <b>Require Encrypted Password</b> check box in the <b>Security</b> dialog box. For more information, see <b>MPRIO_RequireMsEncryptedPw</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireMsEncryptedPw"></a><a id="mprio_requiremsencryptedpw"></a><a id="MPRIO_REQUIREMSENCRYPTEDPW"></a><dl>
<dt><b>MPRIO_RequireMsEncryptedPw</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, only the Microsoft secure password schemes can be used to authenticate the client with the server. This prevents the PPP driver from using the PAP plain-text authentication protocol, MD5-CHAP, or SPAP. For increased security, set this flag. For increased interoperability, clear this flag. This flag takes precedence over 
<b>MPRIO_RequireEncryptedPw</b>.

This flag corresponds to the <b>Require Microsoft Encrypted Password</b> check box in the <b>Security</b> dialog box. For more information, see <b>MPRIO_RequireDataEncryption</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireDataEncryption"></a><a id="mprio_requiredataencryption"></a><a id="MPRIO_REQUIREDATAENCRYPTION"></a><dl>
<dt><b>MPRIO_RequireDataEncryption</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, data encryption must be negotiated successfully or the connection should be dropped. This flag is ignored unless 
<b>MPRIO_RequireMsEncryptedPw</b> is also set.

This flag corresponds to the <b>Require Data Encryption</b> check box in the <b>Security</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_NetworkLogon"></a><a id="mprio_networklogon"></a><a id="MPRIO_NETWORKLOGON"></a><dl>
<dt><b>MPRIO_NetworkLogon</b></dt>
</dl>
</td>
<td width="60%">
This flag is reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_UseLogonCredentials"></a><a id="mprio_uselogoncredentials"></a><a id="MPRIO_USELOGONCREDENTIALS"></a><dl>
<dt><b>MPRIO_UseLogonCredentials</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS uses the user name, password, and domain of the currently logged-on user when dialing this entry. This flag is ignored unless 
<b>MPRIO_RequireMsEncryptedPw</b> is also set.

This setting is ignored by the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function where specifying empty strings for the <b>szUserName</b> and <b>szPassword</b> members of the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure provides the same result.

This flag corresponds to the <b>Use Current Username and Password</b> check box in the <b>Security</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_PromoteAlternates"></a><a id="mprio_promotealternates"></a><a id="MPRIO_PROMOTEALTERNATES"></a><dl>
<dt><b>MPRIO_PromoteAlternates</b></dt>
</dl>
</td>
<td width="60%">
This flag has an effect when alternate phone numbers are defined by the <b>szAlternates</b> member. If this flag is set, an alternate phone number that connects successfully becomes the primary phone number, and the current primary phone number is moved to the alternate list.

This flag corresponds to the check box in the <b>Alternate Numbers</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_SecureLocalFiles"></a><a id="mprio_securelocalfiles"></a><a id="MPRIO_SECURELOCALFILES"></a><dl>
<dt><b>MPRIO_SecureLocalFiles</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, RRAS checks for existing remote file system and remote printer bindings before making a connection with this entry. Typically, you set this flag on phone-book entries for public networks to remind users to break connections to their private network before connecting to a public network.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireEAP"></a><a id="mprio_requireeap"></a><a id="MPRIO_REQUIREEAP"></a><dl>
<dt><b>MPRIO_RequireEAP</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, Extensible Authentication Protocol (EAP) must be supported for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequirePAP"></a><a id="mprio_requirepap"></a><a id="MPRIO_REQUIREPAP"></a><dl>
<dt><b>MPRIO_RequirePAP</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, Password Authentication Protocol must be supported for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireSPAP"></a><a id="mprio_requirespap"></a><a id="MPRIO_REQUIRESPAP"></a><dl>
<dt><b>MPRIO_RequireSPAP</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, Shiva's Password Authentication Protocol (SPAP) must be supported for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_SharedPhoneNumbers"></a><a id="mprio_sharedphonenumbers"></a><a id="MPRIO_SHAREDPHONENUMBERS"></a><dl>
<dt><b>MPRIO_SharedPhoneNumbers</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, phone numbers are shared.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireCHAP"></a><a id="mprio_requirechap"></a><a id="MPRIO_REQUIRECHAP"></a><dl>
<dt><b>MPRIO_RequireCHAP</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the Challenge Handshake Authentication Protocol must be supported for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireMsCHAP"></a><a id="mprio_requiremschap"></a><a id="MPRIO_REQUIREMSCHAP"></a><dl>
<dt><b>MPRIO_RequireMsCHAP</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the Microsoft Challenge Handshake Authentication Protocol must be supported for authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIO_RequireMsCHAP2"></a><a id="mprio_requiremschap2"></a><a id="MPRIO_REQUIREMSCHAP2"></a><dl>
<dt><b>MPRIO_RequireMsCHAP2</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, version 2 of the Microsoft Challenge Handshake Authentication Protocol must be supported for authentication.

</td>
</tr>
</table>

### -field szLocalPhoneNumber

A value that specifies a null-terminated string that contains a telephone number or an IPv6 address.

### -field szAlternates

A pointer to a list of consecutive null-terminated Unicode strings. The last string is terminated by two consecutive null characters. The strings are alternate phone numbers that the router dials, in the order listed, if the primary number fails to connect. For more information, see <b>szLocalPhoneNumber</b>.

### -field ipaddr

A value that specifies the IP address to be used while this connection is active. This member is ignored unless <b>dwfOptions</b> specifies the 
<b>MPRIO_SpecificIpAddr</b> flag.

### -field ipaddrDns

A value that specifies the IP address of the DNS server to be used while this connection is active. This member is ignored unless <b>dwfOptions</b> specifies the 
<b>MPRIO_SpecificNameServers</b> flag.

### -field ipaddrDnsAlt

A value that specifies the IP address of a secondary or backup DNS server to be used while this connection is active. This member is ignored unless <b>dwfOptions</b> specifies the 
<b>MPRIO_SpecificNameServers</b> flag.

### -field ipaddrWins

A value that specifies the IP address of the WINS server to be used while this connection is active. This member is ignored unless <b>dwfOptions</b> specifies the 
<b>MPRIO_SpecificNameServers</b> flag.

### -field ipaddrWinsAlt

A value that specifies the IP address of a secondary WINS server to be used while this connection is active. This member is ignored unless <b>dwfOptions</b> specifies the 
<b>MPRIO_SpecificNameServers</b> flag.

### -field dwfNetProtocols

A value that specifies the network protocols to negotiate. This member can be a combination of the following flags.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRNP_Ipx"></a><a id="mprnp_ipx"></a><a id="MPRNP_IPX"></a><dl>
<dt><b>MPRNP_Ipx</b></dt>
</dl>
</td>
<td width="60%">
Negotiate the IPX protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRNP_Ip"></a><a id="mprnp_ip"></a><a id="MPRNP_IP"></a><dl>
<dt><b>MPRNP_Ip</b></dt>
</dl>
</td>
<td width="60%">
Negotiate the TCP/IP protocol.

</td>
</tr>
</table>
 

<b>64-bit Windows:  </b>The <b>MPRNP_Ipx</b> flag is not supported

### -field szDeviceType

A value that specifies a null-terminated string that indicates the RRAS device type that is referenced by <b>szDeviceName</b>. This member can be one of the following string constants.

<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Modem"></a><a id="mprdt_modem"></a><a id="MPRDT_MODEM"></a><dl>
<dt><b>MPRDT_Modem</b></dt>
</dl>
</td>
<td width="60%">
A modem that is accessed through a COM port.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Isdn"></a><a id="mprdt_isdn"></a><a id="MPRDT_ISDN"></a><dl>
<dt><b>MPRDT_Isdn</b></dt>
</dl>
</td>
<td width="60%">
An ISDN adapter with the corresponding NDISWAN driver installed.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_X25"></a><a id="mprdt_x25"></a><dl>
<dt><b>MPRDT_X25</b></dt>
</dl>
</td>
<td width="60%">
An X.25 adapter with the corresponding NDISWAN driver installed.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Vpn"></a><a id="mprdt_vpn"></a><a id="MPRDT_VPN"></a><dl>
<dt><b>MPRDT_Vpn</b></dt>
</dl>
</td>
<td width="60%">
A virtual private network (VPN) connection.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Pad"></a><a id="mprdt_pad"></a><a id="MPRDT_PAD"></a><dl>
<dt><b>MPRDT_Pad</b></dt>
</dl>
</td>
<td width="60%">
A packet assembler/disassembler.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Generic"></a><a id="mprdt_generic"></a><a id="MPRDT_GENERIC"></a><dl>
<dt><b>MPRDT_Generic</b></dt>
</dl>
</td>
<td width="60%">
Generic.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Serial"></a><a id="mprdt_serial"></a><a id="MPRDT_SERIAL"></a><dl>
<dt><b>MPRDT_Serial</b></dt>
</dl>
</td>
<td width="60%">
Direct serial connection through a serial port.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_FrameRelay"></a><a id="mprdt_framerelay"></a><a id="MPRDT_FRAMERELAY"></a><dl>
<dt><b>MPRDT_FrameRelay</b></dt>
</dl>
</td>
<td width="60%">
Frame Relay.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Atm"></a><a id="mprdt_atm"></a><a id="MPRDT_ATM"></a><dl>
<dt><b>MPRDT_Atm</b></dt>
</dl>
</td>
<td width="60%">
Asynchronous Transfer Mode.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Sonet"></a><a id="mprdt_sonet"></a><a id="MPRDT_SONET"></a><dl>
<dt><b>MPRDT_Sonet</b></dt>
</dl>
</td>
<td width="60%">
Sonet.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_SW56"></a><a id="mprdt_sw56"></a><dl>
<dt><b>MPRDT_SW56</b></dt>
</dl>
</td>
<td width="60%">
Switched 56K Access.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Irda"></a><a id="mprdt_irda"></a><a id="MPRDT_IRDA"></a><dl>
<dt><b>MPRDT_Irda</b></dt>
</dl>
</td>
<td width="60%">
An Infrared Data Association (IrDA)-compliant device.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDT_Parallel"></a><a id="mprdt_parallel"></a><a id="MPRDT_PARALLEL"></a><dl>
<dt><b>MPRDT_Parallel</b></dt>
</dl>
</td>
<td width="60%">
Direct parallel connection through a parallel port.

</td>
</tr>
</table>

### -field szDeviceName

Contains a null-terminated string that contains the name of a TAPI device to use with this phone-book entry, for example, "Fabrikam Inc 28800 External". To enumerate all available RAS-capable devices, use the 
<a href="/windows/desktop/api/ras/nf-ras-rasenumdevicesa">RasEnumDevices</a> function.

### -field szX25PadType

A data type that contains a null-terminated string that identifies the X.25 PAD type. Set this member to an empty string ("") unless the entry should dial using an X.25 PAD.

<b>Windows 2000 and Windows NT:  </b>The <b>szX25PadType</b> string maps to a section name in PAD.INF.

### -field szX25Address

Contains a null-terminated string that identifies the X.25 address to connect to. Set this member to an empty string ("") unless the entry should dial using an X.25 PAD or native X.25 device.

### -field szX25Facilities

Contains a null-terminated string that specifies the facilities to request from the X.25 host at connection time. This member is ignored if <b>szX25Address</b> is an empty string ("").

### -field szX25UserData

Contains a null-terminated string that specifies additional connection data supplied to the X.25 host at connection time. This member is ignored if <b>szX25Address</b> is an empty string ("").

### -field dwChannels

Reserved for future use.

### -field dwSubEntries

A value that specifies the number of multilink subentries associated with this entry. When calling 
<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a>, set this member to zero. To add subentries to a phone-book entry, use the 
<a href="/windows/desktop/api/ras/nf-ras-rassetsubentrypropertiesa">RasSetSubEntryProperties</a> function.

### -field dwDialMode

Indicates whether RRAS should dial all of this entry's multilink subentries when the entry is first connected. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRDM_DialAll"></a><a id="mprdm_dialall"></a><a id="MPRDM_DIALALL"></a><dl>
<dt><b>MPRDM_DialAll</b></dt>
</dl>
</td>
<td width="60%">
Dial all subentries initially.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRDM_DialAsNeeded"></a><a id="mprdm_dialasneeded"></a><a id="MPRDM_DIALASNEEDED"></a><dl>
<dt><b>MPRDM_DialAsNeeded</b></dt>
</dl>
</td>
<td width="60%">
Adjust the number of subentries as bandwidth is required. RRAS uses the <b>dwDialExtraPercent</b>, <b>dwDialExtraSampleSeconds</b>, <b>dwDialHangUpExtraPercent</b>, and <b>dwHangUpExtraSampleSeconds</b> members to determine when to dial or disconnect a subentry.

</td>
</tr>
</table>

### -field dwDialExtraPercent

A value that specifies the percentage of the total bandwidth that is available from the currently connected subentries. RRAS dials an additional subentry when the total bandwidth that is used exceeds <b>dwDialExtraPercent</b> percent of the available bandwidth for at least <b>dwDialExtraSampleSeconds</b> seconds.

This member is ignored unless the <b>dwDialMode</b> member specifies the <b>MPRDM_DialAsNeeded</b> flag.

### -field dwDialExtraSampleSeconds

A value that specifies the time, in seconds, for which current bandwidth usage must exceed the threshold that is specified by <b>dwDialExtraPercent</b> before RRAS dials an additional subentry.

This member is ignored unless the <b>dwDialMode</b> member specifies the <b>MPRDM_DialAsNeeded</b> flag.

### -field dwHangUpExtraPercent

A value that specifies the percentage of the total bandwidth that is available from the currently connected subentries. RRAS terminates (hangs up) an existing subentry connection when the total bandwidth used is less than <b>dwHangUpExtraPercent</b> percent of the available bandwidth for at least <b>dwHangUpExtraSampleSeconds</b> seconds.

This member is ignored unless the <b>dwDialMode</b> member specifies the <b>MPRDM_DialAsNeeded</b> flag.

### -field dwHangUpExtraSampleSeconds

A value that specifies the time, in seconds, for which current bandwidth usage must be less than the threshold that is specified by <b>dwHangUpExtraPercent</b> before RRAS terminates an existing subentry connection.

This member is ignored unless the <b>dwDialMode</b> member specifies the <b>MPRDM_DialAsNeeded</b> flag.

### -field dwIdleDisconnectSeconds

A value that specifies the time, in seconds, after which an inactive connection is terminated. Unless the idle time-out is disabled, the entire connection is terminated if the connection is idle for the specified interval. This member can specify either a time-out value, or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRIDS_Disabled"></a><a id="mprids_disabled"></a><a id="MPRIDS_DISABLED"></a><dl>
<dt><b>MPRIDS_Disabled</b></dt>
</dl>
</td>
<td width="60%">
There is no idle time-out for this connection.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRIDS_UseGlobalValue"></a><a id="mprids_useglobalvalue"></a><a id="MPRIDS_USEGLOBALVALUE"></a><dl>
<dt><b>MPRIDS_UseGlobalValue</b></dt>
</dl>
</td>
<td width="60%">
Use the user preference value as the default.

</td>
</tr>
</table>

### -field dwType

A value that specifies the type of phone-book entry. This member can be one of the following types.

<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRET_Phone"></a><a id="mpret_phone"></a><a id="MPRET_PHONE"></a><dl>
<dt><b>MPRET_Phone</b></dt>
</dl>
</td>
<td width="60%">
Phone line, for example, modem, ISDN, or X.25.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRET_Vpn"></a><a id="mpret_vpn"></a><a id="MPRET_VPN"></a><dl>
<dt><b>MPRET_Vpn</b></dt>
</dl>
</td>
<td width="60%">
Virtual Private Network.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRET_Direct"></a><a id="mpret_direct"></a><a id="MPRET_DIRECT"></a><dl>
<dt><b>MPRET_Direct</b></dt>
</dl>
</td>
<td width="60%">
Direct serial or parallel connection.

</td>
</tr>
</table>

### -field dwEncryptionType

A value that specifies the type of encryption to use for Microsoft Point-to-Point Encryption (MPPE) with the connection. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_ET_None"></a><a id="mpr_et_none"></a><a id="MPR_ET_NONE"></a><dl>
<dt><b>MPR_ET_None</b></dt>
</dl>
</td>
<td width="60%">
Do not use encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ET_Require"></a><a id="mpr_et_require"></a><a id="MPR_ET_REQUIRE"></a><dl>
<dt><b>MPR_ET_Require</b></dt>
</dl>
</td>
<td width="60%">
Use encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ET_RequireMax"></a><a id="mpr_et_requiremax"></a><a id="MPR_ET_REQUIREMAX"></a><dl>
<dt><b>MPR_ET_RequireMax</b></dt>
</dl>
</td>
<td width="60%">
Use maximum-strength encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_ET_Optional"></a><a id="mpr_et_optional"></a><a id="MPR_ET_OPTIONAL"></a><dl>
<dt><b>MPR_ET_Optional</b></dt>
</dl>
</td>
<td width="60%">
If possible, use encryption. 

</td>
</tr>
</table>
 

The value of <b>dwEncryptionType</b> does not affect how passwords are encrypted. Whether passwords are encrypted and how passwords are encrypted is determined by the authentication protocol, for example, PAP, MS-CHAP, or EAP.

### -field dwCustomAuthKey

A value that specifies the authentication key to be provided to an Extensible Authentication Protocol (EAP) vendor.

### -field dwCustomAuthDataSize

A value that specifies the size of the data pointed to by the <b>lpbCustomAuthData</b> member.

### -field lpbCustomAuthData

A pointer to authentication data to use with EAP.

### -field guidId

The globally unique identifier (GUID) that represents this phone-book entry. This member is read-only.

### -field dwVpnStrategy

The VPN strategy to use when dialing a VPN connection. This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPR_VS_Default"></a><a id="mpr_vs_default"></a><a id="MPR_VS_DEFAULT"></a><dl>
<dt><b>MPR_VS_Default</b></dt>
</dl>
</td>
<td width="60%">
RRAS dials PPTP first. If PPTP fails, L2TP is attempted. The protocol that succeeds is tried first in subsequent dialing for this entry.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_VS_PptpOnly"></a><a id="mpr_vs_pptponly"></a><a id="MPR_VS_PPTPONLY"></a><dl>
<dt><b>MPR_VS_PptpOnly</b></dt>
</dl>
</td>
<td width="60%">
RAS dials only PPTP.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_VS_PptpFirst"></a><a id="mpr_vs_pptpfirst"></a><a id="MPR_VS_PPTPFIRST"></a><dl>
<dt><b>MPR_VS_PptpFirst</b></dt>
</dl>
</td>
<td width="60%">
RAS always dials PPTP first, L2TP second.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_VS_L2tpOnly"></a><a id="mpr_vs_l2tponly"></a><a id="MPR_VS_L2TPONLY"></a><dl>
<dt><b>MPR_VS_L2tpOnly</b></dt>
</dl>
</td>
<td width="60%">
RAS dials only L2TP.

</td>
</tr>
<tr>
<td width="40%"><a id="MPR_VS_L2tpFirst"></a><a id="mpr_vs_l2tpfirst"></a><a id="MPR_VS_L2TPFIRST"></a><dl>
<dt><b>MPR_VS_L2tpFirst</b></dt>
</dl>
</td>
<td width="60%">
RAS dials L2TP first, PPTP second.

</td>
</tr>
</table>

### -field AddressCount

Not used.

### -field ipv6addrDns

A value that specifies the IP address of the DNS server to be used while this connection is active.

### -field ipv6addrDnsAlt

A value that specifies the IP address of a secondary or backup DNS server to be used while this connection is active.

### -field ipv6addr

Not used.

## -remarks

The 
<b>MPR_INTERFACE_3</b> structure has a number of members that are similar to members of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure. 

The following members from the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure have no counterpart in 
<b>MPR_INTERFACE_3</b>:

<ul>
<li><b>dwCountryID</b></li>
<li><b>dwCountryCode</b></li>
<li><b>szAreaCode</b></li>
<li><b>dwFramingProtocol</b></li>
</ul>
<b>64-bit Windows:  </b>Does not support the IPX protocol.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_1">MPR_INTERFACE_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacesetinfo">MprAdminInterfaceSetInfo</a>
