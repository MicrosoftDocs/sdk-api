---
UID: NS:tcpioctl.IFEntry
title: IFEntry (tcpioctl.h)
description: Describes a TCP/IP interface in accord with the Simple Network Management Protocol, version 2, (SNMPv2) standard for Management Information Base for network management of TCP/IP networks (MIB-II), as specified in the Internet Engineering Task Force (IETF) Request for Comments (RFC) 1213 on pages 16 through 23.
helpviewer_keywords: ["IFEntry","IFEntry structure [Windows API]","tcpioctl/IFEntry","winprog.ifentry"]
old-location: winprog\ifentry.htm
tech.root: winprog
ms.assetid: 830cd19e-06a9-46dc-a869-d2a17107d942
ms.date: 12/05/2018
ms.keywords: IFEntry, IFEntry structure [Windows API], tcpioctl/IFEntry, winprog.ifentry
req.header: tcpioctl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IFEntry
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFEntry
 - tcpioctl/IFEntry
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
 - IFEntry
---

# IFEntry structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Describes a TCP/IP interface in accord with 
				the Simple Network Management Protocol, version 2, (SNMPv2) standard for Management Information Base for network management 
				of TCP/IP networks (MIB-II), as specified in the Internet Engineering Task Force (IETF) Request for Comments 
				<a href="https://www.ietf.org/rfc/rfc1213.txt">(RFC) 1213</a> on pages 16 through 23.

## -struct-fields

### -field if_index

A value between 1 and the number of network interfaces present on this system,  regardless of
							their current state, that  uniquely  identifies this interface and persists across reinitialization 
							of the network management system.

### -field if_type

The interface type according to
						the physical or link protocol(s) immediately below the network layer in the protocol 
						stack. The following table lists the possible values of this <b>if_type</b> 
						member enumerated on pages  18 and 19 of 
						<a href="https://www.ietf.org/rfc/rfc1213.txt">RFC 1213</a>.

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
other (that is, none of the following)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
regular1822

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
hdh1822

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
ddn-x25

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
rfc877-x25

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Ethernet-csmacd

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
iso88023-csmacd

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
iso88024-tokenBus

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9</dt>
</dl>
</td>
<td width="60%">
iso88025-tokenRing

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
iso88026-man

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
starLan

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>12</dt>
</dl>
</td>
<td width="60%">
proteon-10Mbit

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>13</dt>
</dl>
</td>
<td width="60%">
proteon-80Mbit

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>14</dt>
</dl>
</td>
<td width="60%">
hyperchannel

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>15</dt>
</dl>
</td>
<td width="60%">
fddi

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16</dt>
</dl>
</td>
<td width="60%">
lapb

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>17</dt>
</dl>
</td>
<td width="60%">
sdlc

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>18</dt>
</dl>
</td>
<td width="60%">
ds1 (T-1)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>19</dt>
</dl>
</td>
<td width="60%">
e1 (European equiv. of T-1)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>20</dt>
</dl>
</td>
<td width="60%">
basicISDN

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>21</dt>
</dl>
</td>
<td width="60%">
primaryISDN (proprietary serial)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>22</dt>
</dl>
</td>
<td width="60%">
propPointToPointSerial

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>23</dt>
</dl>
</td>
<td width="60%">
ppp

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>24</dt>
</dl>
</td>
<td width="60%">
softwareLoopback

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>25</dt>
</dl>
</td>
<td width="60%">
eon (CLNP over IP [11])

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>26</dt>
</dl>
</td>
<td width="60%">
Ethernet-3Mbit

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>27</dt>
</dl>
</td>
<td width="60%">
nsip (XNS over IP)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>28</dt>
</dl>
</td>
<td width="60%">
slip (generic SLIP)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>29</dt>
</dl>
</td>
<td width="60%">
ultra (ULTRA technologies)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30</dt>
</dl>
</td>
<td width="60%">
ds3 (T-3)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>31</dt>
</dl>
</td>
<td width="60%">
sip (SMDS)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>32</dt>
</dl>
</td>
<td width="60%">
frame-relay(32)

</td>
</tr>
</table>
 

Include the Ipifcons.h header file from the Microsoft SDK for flag constants supporting these and additional IP interface types.

When you examine the value of the <b>if_type</b> member, you may also want to define and test for an additional constant that identifies a "loopback" interface: <code>#define IF_TYPE_LOOPBACK   0</code>

### -field if_mtu

The size, in bytes, of the largest datagram that can be sent or received on the interface.
						For interfaces that are used to transmit network datagrams, this is the size of the largest 
						network datagram that can be sent on the interface.

### -field if_speed

An estimate of the interface's current bandwidth, in bits per second. For interfaces that do not
						vary in bandwidth or for which no accurate estimation can be made, this member contains the nominal bandwidth.

### -field if_physaddrlen

The length, in bytes, of the address contained in the <b>if_physaddr</b> member. 
					For interfaces such as serial ports that do not have an address of this kind, the <b>if_physaddrlen</b> member is zero.

### -field if_physaddr

The interface's address at the protocol layer immediately below the network layer in the protocol stack.
				For interfaces such as serial ports that do not have an address of this kind, the <b>if_physaddr</b> 
				member contains an empty string.

### -field if_adminstatus

The desired state of the interface; one of the following values specified on page 20 of 
						<a href="https://www.ietf.org/rfc/rfc1213.txt">RFC 1213</a>.
					
			 

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
Up; ready to pass packets.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
In a test state, such that no operational packets can be passed.

</td>
</tr>
</table>

### -field if_operstatus

The actual current operational state of the interface; one of the following values specified on page 20 of 
						<a href="https://www.ietf.org/rfc/rfc1213.txt">RFC 1213</a>.
					
				 

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
Up; ready to pass packets.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
In a test state, such that no operational packets can be passed.

</td>
</tr>
</table>

### -field if_lastchange

The time, in hundredths of a second, since the network management portion of the system was last
						reinitialized, at which this interface entered its actual current operational 
						state. If the current state was entered prior to the last reinitialization of 
						the local network management subsystem, this member is set to zero.

### -field if_inoctets

The total number of bytes received on this interface, including framing characters.

### -field if_inucastpkts

The number of subnetwork unicast packets delivered to a higher-layer protocol.

### -field if_innucastpkts

The number of non-unicast (subnetwork broadcast or subnetwork multicast) 
						packets delivered to a higher-layer protocol.

### -field if_indiscards

The number of inbound packets that have been discarded to free up memory resources
						or for other similar reason not related to any error that would prevent their being 
						deliverable to a higher-layer protocol.

### -field if_inerrors

The number of inbound packets that have contained errors that prevent them from being 
						deliverable to a higher-layer protocol.

### -field if_inunknownprotos

The number of inbound packets that have been discarded because of an unknown or 
						unsupported protocol.

### -field if_outoctets

The total number of bytes transmitted out of the interface, including framing characters.

### -field if_outucastpkts

The total number of packets that higher-level protocols have requested be transmitted 
						to a subnetwork unicast address, including those that were discarded or not sent.

### -field if_outnucastpkts

The total number of packets that higher-level protocols have requested be 
						transmitted to a non-unicast (subnetwork broadcast or subnetwork 
						multicast) address, including those that were discarded or not sent.

### -field if_outdiscards

The number of outbound packets that have been discarded to free up 
						memory resources or for other similar reasons not related to any 
						error that would prevent their being transmitted.

### -field if_outerrors

The number of outbound packets that could not be transmitted because of errors.

### -field if_outqlen

The current number of packets in the output packet queue.

### -field if_descrlen

The size, in bytes, not counting any terminating null character, of the interface 
						description text contained in the <b>if_descr</b> member.

### -field if_descr

A text string that contains information about this interface, 
						including the manufacturer's name, product name, and hardware version. 
						If the string is not included, the size of the buffer is 1 byte.

## -remarks

Because of its variable-length <b>if_descr</b> member, 
				the <b>IFEntry</b> structure does not have a fixed size. 
				For purposes of allocating memory to contain an actual instance of the structure, 
				a reasonably safe buffer size can be computed as follows:
			

<code>maxIFEntryLen = sizeof(IFEntry) + MAX_ADAPTER_DESCRIPTION_LENGTH + 1;</code>

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">Management Information Base
			 Reference</a>