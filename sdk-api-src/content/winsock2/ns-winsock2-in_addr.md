---
UID: NS:winsock2.in_addr
title: in_addr (winsock2.h)
description: The in_addr structure represents an IPv4 Internet address.
helpviewer_keywords: ["FAR *LPIN_ADDR","FAR *LPIN_ADDR structure [Winsock]","IN_ADDR","IN_ADDR [Winsock]","IN_ADDR structure [Winsock]","PIN_ADDR","PIN_ADDR structure pointer [Winsock]","_win32_in_addr_2","in_addr","in_addr structure [Winsock]","inaddr/FAR *LPIN_ADDR","inaddr/PIN_ADDR","inaddr/in_addr","winsock.in_addr_2","winsock2/FAR *LPIN_ADDR","winsock2/PIN_ADDR","winsock2/in_addr"]
old-location: winsock\in_addr_2.htm
tech.root: WinSock
ms.assetid: fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c
ms.date: 12/05/2018
ms.keywords: FAR *LPIN_ADDR, FAR *LPIN_ADDR structure [Winsock], IN_ADDR, IN_ADDR [Winsock], IN_ADDR structure [Winsock], PIN_ADDR, PIN_ADDR structure pointer [Winsock], _win32_in_addr_2, in_addr, in_addr structure [Winsock], inaddr/FAR *LPIN_ADDR, inaddr/PIN_ADDR, inaddr/in_addr, winsock.in_addr_2, winsock2/FAR *LPIN_ADDR, winsock2/PIN_ADDR, winsock2/in_addr
req.header: winsock2.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - in_addr
 - winsock2/in_addr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Inaddr.h
 - Winsock2.h
api_name:
 - IN_ADDR
---

# in_addr structure


## -description

The 
<b>in_addr</b> structure represents an IPv4 Internet address.

## -struct-fields

### -field S_un

### -field S_un.S_un_b

An IPv4 address formatted as four <b>u_char</b>s.

### -field S_un.S_un_b.s_b1

### -field S_un.S_un_b.s_b2

### -field S_un.S_un_b.s_b3

### -field S_un.S_un_b.s_b4

### -field S_un.S_un_w

An IPv4 address formatted as two <b>u_short</b>s.

### -field S_un.S_un_w.s_w1

### -field S_un.S_un_w.s_w2

### -field S_un.S_addr

An IPv4 address formatted as a <b>u_long</b>.

## -remarks

The <b>in_addr</b> structure is used with IPv4 addresses. 

The <b>in_addr</b> structure is the IPv4 equivalent of the IPv6-based <a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">in6_addr</a> structure.  

<div class="alert"><b>Note</b>  The <b>IN_ADDR</b>, <b>PIN_ADDR</b>, and  <b>LPIN_ADDR</b> derived structures are only defined on the Windows SDK released with Windows Vista and later. The <b>IN_ADDR</b>, <b>PIN_ADDR</b>, and  <b>LPIN_ADDR</b> derived structures are defined in the <i>Inaddr.h</i> header file. On earlier versions of the Windows SDK, variables of this type should be declared as <b>struct in_addr</b>. </div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)">in6_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>