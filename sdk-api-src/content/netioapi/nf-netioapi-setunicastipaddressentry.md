---
UID: NF:netioapi.SetUnicastIpAddressEntry
title: SetUnicastIpAddressEntry function (netioapi.h)
description: Sets the properties of an existing unicast IP address entry on the local computer.
helpviewer_keywords: ["SetUnicastIpAddressEntry","SetUnicastIpAddressEntry function [IP Helper]","iphlp.setunicastipaddressentry","netioapi/SetUnicastIpAddressEntry"]
old-location: iphlp\setunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: 906a3895-2e42-4bed-90a3-7c10487d76cb
ms.date: 12/05/2018
ms.keywords: SetUnicastIpAddressEntry, SetUnicastIpAddressEntry function [IP Helper], iphlp.setunicastipaddressentry, netioapi/SetUnicastIpAddressEntry
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetUnicastIpAddressEntry
 - netioapi/SetUnicastIpAddressEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - SetUnicastIpAddressEntry
---

# SetUnicastIpAddressEntry function


## -description

The 
<a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function  sets the properties of  an existing unicast IP address entry on the local computer.

## -parameters

### -param Row [in]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry for an existing unicast IP address entry.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter was not set to a valid unicast IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_UNICASTIPADDRESS_ROW</b> pointed to by the <i>Row</i> parameter were unspecified.

This error is also returned for other errors in the values set for members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. These errors include the following: if the <b>ValidLifetime</b> member is less than the <b>PreferredLifetime</b> member, if the <b>PrefixOrigin</b> member is set to <b>IpPrefixOriginUnchanged</b> and the <b>SuffixOrigin</b> is the not set to <b>IpSuffixOriginUnchanged</b>, if the <b>PrefixOrigin</b> member is not set to <b>IpPrefixOriginUnchanged</b> and the <b>SuffixOrigin</b> is set to <b>IpSuffixOriginUnchanged</b>, if the <b>PrefixOrigin</b> member is not set to a value from the <b>NL_PREFIX_ORIGIN</b> enumeration, if the <b>SuffixOrigin</b> member is not set to a value from the <b>NL_SUFFIX_ORIGIN</b> enumeration, or if the <b>OnLinkPrefixLength</b> member is set to a value greater than the IP address length, in bits (32 for an unicast IPv4 address or 128 for an unicast IPv6 address).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <b>Address</b> member <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter or no IPv6 stack is on the local computer and an IPv6 address was specified in the <b>Address</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function is defined on Windows Vista and later. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> function is normally used to retrieve an existing <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry to be modified.  An application can then change the
    members in the <b>MIB_UNICASTIPADDRESS_ROW</b> entry it wishes to modify, and then call the <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function. 

An application may call the <a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a> function to initialize the members of a
    <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry with default values before making changes. However, the application would normally save either the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member before calling <b>InitializeUnicastIpAddressEntry</b> and restore one of these members after the call. 

The <b>Address</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid unicast IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

If the <b>OnLinkPrefixLength</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is set to 255, then <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> will set the unicast IP address properties so that the <b>OnLinkPrefixLength</b> member is equal to the length of the IP address. So for a unicast IPv4 address, the  <b>OnLinkPrefixLength</b> is set to 32 and the <b>OnLinkPrefixLength</b> is set to 128 for a unicast IPv6 address. If this would result in the incorrect subnet mask for an IPv4 address or the incorrect link prefix for an IPv6 address, then the application should set this member to the correct value before calling <b>SetUnicastIpAddressEntry</b>. 

The <b>DadState</b>, <b>ScopeId</b>, and <b>CreationTimeStamp</b> members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> are ignored when the  <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a>  function is called. These members are set by the network stack and cannot be changed using the <b>SetUnicastIpAddressEntry</b>  function. The  <b>ScopeId</b> member is automatically determined by the interface on which the address was added.

The <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function can only be called by a user logged on as a member of the Administrators group. If <b>SetUnicastIpAddressEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteunicastipaddressentry">DeleteUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>