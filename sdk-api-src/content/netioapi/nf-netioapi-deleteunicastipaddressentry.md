---
UID: NF:netioapi.DeleteUnicastIpAddressEntry
title: DeleteUnicastIpAddressEntry function (netioapi.h)
description: Deletes an existing unicast IP address entry on the local computer.
helpviewer_keywords: ["DeleteUnicastIpAddressEntry","DeleteUnicastIpAddressEntry function [IP Helper]","iphlp.deleteunicastipaddressentry","netioapi/DeleteUnicastIpAddressEntry"]
old-location: iphlp\deleteunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: a630397a-ef4a-40c2-b2e7-3e85cd9e8029
ms.date: 12/05/2018
ms.keywords: DeleteUnicastIpAddressEntry, DeleteUnicastIpAddressEntry function [IP Helper], iphlp.deleteunicastipaddressentry, netioapi/DeleteUnicastIpAddressEntry
f1_keywords:
- netioapi/DeleteUnicastIpAddressEntry
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iphlpapi.dll
api_name:
- DeleteUnicastIpAddressEntry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteUnicastIpAddressEntry function


## -description


The 
<b>DeleteUnicastIpAddressEntry</b> function   deletes an existing unicast IP address entry on the local computer. 


## -parameters




### -param Row [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry for an existing unicast IP address entry to delete from the local computer.


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter was not set to a valid unicast IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_UNICASTIPADDRESS_ROW</b> pointed to by the <i>Row</i> parameter were unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <b>Address</b> member <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address was specified in the <b>Address</b> member.

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
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>DeleteUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>DeleteUnicastIpAddressEntry</b> function is used to delete an existing <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry on the local computer.  

On input, the <b>Address</b> member in the <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter must be set to a valid unicast IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

If the function is successful, the existing IP address represented by the <i>Row</i> parameter was deleted. 

The <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> function can be called to enumerate the unicast IP address entries on a local computer. The <a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> function can be called to retrieve a specific existing unicast IP address entry.

The <b>DeleteUnicastIpAddressEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeleteUnicastIpAddressEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="https://docs.microsoft.com/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>
 

 

