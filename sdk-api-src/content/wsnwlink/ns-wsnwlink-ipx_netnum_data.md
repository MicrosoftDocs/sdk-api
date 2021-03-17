---
UID: NS:wsnwlink._IPX_NETNUM_DATA
title: IPX_NETNUM_DATA (wsnwlink.h)
description: The IPX_NETNUM_DATA structure provides information about a specified IPX network number. Used in conjunction with getsockopt function calls that specify IPX_GETNETINFO in the optname parameter.
helpviewer_keywords: ["*PIPX_NETNUM_DATA","IPX_NETNUM_DATA","IPX_NETNUM_DATA structure [Winsock]","PIPX_NETNUM_DATA","PIPX_NETNUM_DATA structure pointer [Winsock]","_win32_ipx_netnum_data_2","winsock.ipx_netnum_data_2","wsnwlink/IPX_NETNUM_DATA","wsnwlink/PIPX_NETNUM_DATA"]
old-location: winsock\ipx_netnum_data_2.htm
tech.root: WinSock
ms.assetid: 9ac7f6ea-5ed3-45f9-8422-62fef1681cdc
ms.date: 12/05/2018
ms.keywords: '*PIPX_NETNUM_DATA, IPX_NETNUM_DATA, IPX_NETNUM_DATA structure [Winsock], PIPX_NETNUM_DATA, PIPX_NETNUM_DATA structure pointer [Winsock], _win32_ipx_netnum_data_2, winsock.ipx_netnum_data_2, wsnwlink/IPX_NETNUM_DATA, wsnwlink/PIPX_NETNUM_DATA'
req.header: wsnwlink.h
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
req.typenames: IPX_NETNUM_DATA, *PIPX_NETNUM_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_NETNUM_DATA
 - wsnwlink/_IPX_NETNUM_DATA
 - PIPX_NETNUM_DATA
 - wsnwlink/PIPX_NETNUM_DATA
 - IPX_NETNUM_DATA
 - wsnwlink/IPX_NETNUM_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsnwlink.h
api_name:
 - IPX_NETNUM_DATA
---

# IPX_NETNUM_DATA structure


## -description

The 
<b>IPX_NETNUM_DATA</b> structure provides information about a specified IPX network number. Used in conjunction with 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function calls that specify IPX_GETNETINFO in the <i>optname</i> parameter.

## -struct-fields

### -field netnum

IPX network number for which information is being requested.

### -field hopcount

Number of hops to the IPX network being queried, in machine order.

### -field netdelay

Network delay tick count required to reach the IPX network, in machine order.

### -field cardnum

Adapter number used to reach the IPX network. The adapter number is zero based, such that if eight adapters are on a given computer, they are numbered 0-7.

### -field router

Media Access Control (MAC) address of the next-hop router in the path between the computer and the IPX network. This value is zero if the computer is directly attached to the IPX network.

## -remarks

If information about the IPX network is in the computer's IPX cache, the call will return immediately. If not, RIP requests are used to resolve the information.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>