---
UID: NS:tcpioctl.IPInterfaceInfo
title: IPInterfaceInfo (tcpioctl.h)
description: The IPInterfaceInfo structure contains information about a specific IP interface, returned by the IOCTL_TCP_QUERY_INFORMATION_EX control code.
helpviewer_keywords: ["IPInterfaceInfo","IPInterfaceInfo structure [Windows API]","tcpioctl/IPInterfaceInfo","winprog.ipinterfaceinfo"]
old-location: winprog\ipinterfaceinfo.htm
tech.root: winprog
ms.assetid: dc9de369-f739-475c-96f5-e2e058705fe8
ms.date: 12/05/2018
ms.keywords: IPInterfaceInfo, IPInterfaceInfo structure [Windows API], tcpioctl/IPInterfaceInfo, winprog.ipinterfaceinfo
req.header: tcpioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: IPInterfaceInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPInterfaceInfo
 - tcpioctl/IPInterfaceInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpioctl.h
api_name:
 - IPInterfaceInfo
---

# IPInterfaceInfo structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

The <b>IPInterfaceInfo</b> structure contains information about a specific IP interface, returned by the <a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.

## -struct-fields

### -field iii_flags

The types of communication supported on this interface. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Point-to-point.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Point-to-multipoint.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Unidirectional communication.

</td>
</tr>
</table>

### -field iii_mtu

The maximum transmission unit: the size, in bytes, of the largest datagram that can be sent 
					and/or received on the interface.

### -field iii_speed

An estimate of the interface's current bandwidth in bits per second. For interfaces that 
					do not vary in bandwidth or for which no accurate estimation can be made, this member contains 
					the nominal bandwidth.

### -field iii_addrlength

The length, in bytes, of the IP address associated with this interface that is contained in the 
					<b>iii_addr</b> member.

### -field iii_addr

The IP address associated with this interface. In Windows Vista, this is the physical address.

## -remarks

This is a variable-length structure whose size depends on whether the <b>iii_addr</b> member contains an IPv4 or IPv6 address. To allocate a buffer large enough to contain it safely, use the size: 

<code>sizeof(IPInterfaceInfo) + MAX_PHYSADDR_SIZE</code>

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">Management Information Base
			 Reference</a>