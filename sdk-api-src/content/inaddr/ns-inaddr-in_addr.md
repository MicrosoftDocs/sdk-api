---
UID: NS:inaddr.in_addr
title: IN_ADDR (inaddr.h)
description: The in_addr structure represents an IPv4 address.
helpviewer_keywords: ["*LPIN_ADDR","*PIN_ADDR","IN_ADDR","IPAddr","IPAddr structure [IP Helper]","in_addr","in_addr structure [IP Helper]","inaddr/in_addr","ipexport/in_addr","iphlp.ipaddr"]
old-location: iphlp\ipaddr.htm
tech.root: IpHlp
ms.assetid: 00d4823d-114d-4cc7-afdf-54c7fed3fe45
ms.date: 12/05/2018
ms.keywords: '*LPIN_ADDR, *PIN_ADDR, IN_ADDR, IPAddr, IPAddr structure [IP Helper], in_addr, in_addr structure [IP Helper], inaddr/in_addr, ipexport/in_addr, iphlp.ipaddr'
req.header: inaddr.h
req.include-header: Ipexport.h
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
req.typenames: IN_ADDR, *PIN_ADDR, *LPIN_ADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - in_addr
 - inaddr/in_addr
 - PIN_ADDR
 - inaddr/PIN_ADDR
 - IN_ADDR
 - inaddr/IN_ADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Inaddr.h
 - Ipexport.h
api_name:
 - IPAddr
---

# IN_ADDR structure


## -description

The <b>in_addr</b> structure represents an IPv4 address.
<div class="alert"><b>Note</b>  The <b>IPaddr</b> type definition in IP Helper also represents an IPv4 address and can be cast to an interchangeable <a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a> structure when needed. The <b>in_addr</b> structure in IP Helper has the same syntax and usage as the Windows Sockets <b>in_addr</b> structure, and is interchangeable with <b>in_addr</b> structure used in Windows sockets. Windows sockets also defines an <b>IN_ADDR</b> typedef for the <b>in_addr</b> structure.</div><div> </div>

## -struct-fields

### -field S_un

### -field S_un.S_un_b

The IPv4 address of the host formatted as four <b>u_char</b>s.

### -field S_un.S_un_b.s_b1

### -field S_un.S_un_b.s_b2

### -field S_un.S_un_b.s_b3

### -field S_un.S_un_b.s_b4

### -field S_un.S_un_w

The IPv4 address of the host formatted as two <b>u_short</b>s.

### -field S_un.S_un_w.s_w1

### -field S_un.S_un_w.s_w2

### -field S_un.S_addr

Address of the host formatted as a <b>u_long</b>.

## -remarks

The <b>IPaddr</b> type definition also represents an IPv4 address and can be cast to an  <b>in_addr</b> structure when needed.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>in_addr</b> structure is defined in the <i>Inaddr.h</i> header file which is automatically included by the <i>Ipexport.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>in_addr</b> structure is declared in the <i>Ipexport.h</i> header file.

## -see-also

<a href="/windows/desktop/api/ipexport/ns-ipexport-arp_send_reply">ARP_SEND_REPLY</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getrttandhopcount">GetRTTAndHopCount</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-icmp_echo_reply">ICMP_ECHO_REPLY</a>



<a href="/windows/win32/api/ipexport/ns-ipexport-ip_unidirectional_adapter_address">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho">IcmpSendEcho</a>



<a href="/windows/desktop/api/icmpapi/nf-icmpapi-icmpsendecho2">IcmpSendEcho2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-sendarp">SendARP</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr(Winsock)</a>