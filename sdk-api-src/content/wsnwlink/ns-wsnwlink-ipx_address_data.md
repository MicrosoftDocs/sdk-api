---
UID: NS:wsnwlink._IPX_ADDRESS_DATA
title: IPX_ADDRESS_DATA (wsnwlink.h)
description: The IPX_ADDRESS_DATA structure provides information about a specific adapter to which IPX is bound. Used in conjunction with getsockopt function calls that specify IPX_ADDRESS in the optname parameter.
helpviewer_keywords: ["*PIPX_ADDRESS_DATA","IPX_ADDRESS_DATA","IPX_ADDRESS_DATA structure [Winsock]","PIPX_ADDRESS_DATA","PIPX_ADDRESS_DATA structure pointer [Winsock]","_win32_ipx_address_data_2","winsock.ipx_address_data_2","wsnwlink/IPX_ADDRESS_DATA","wsnwlink/PIPX_ADDRESS_DATA"]
old-location: winsock\ipx_address_data_2.htm
tech.root: WinSock
ms.assetid: 8e18ee5a-04fd-4efc-8d0c-e4ff04fd9f1b
ms.date: 12/05/2018
ms.keywords: '*PIPX_ADDRESS_DATA, IPX_ADDRESS_DATA, IPX_ADDRESS_DATA structure [Winsock], PIPX_ADDRESS_DATA, PIPX_ADDRESS_DATA structure pointer [Winsock], _win32_ipx_address_data_2, winsock.ipx_address_data_2, wsnwlink/IPX_ADDRESS_DATA, wsnwlink/PIPX_ADDRESS_DATA'
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
req.typenames: IPX_ADDRESS_DATA, *PIPX_ADDRESS_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_ADDRESS_DATA
 - wsnwlink/_IPX_ADDRESS_DATA
 - PIPX_ADDRESS_DATA
 - wsnwlink/PIPX_ADDRESS_DATA
 - IPX_ADDRESS_DATA
 - wsnwlink/IPX_ADDRESS_DATA
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
 - IPX_ADDRESS_DATA
---

# IPX_ADDRESS_DATA structure


## -description

The 
<b>IPX_ADDRESS_DATA</b> structure provides information about a specific adapter to which IPX is bound. Used in conjunction with 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function calls that specify IPX_ADDRESS in the <i>optname</i> parameter.

## -struct-fields

### -field adapternum

0-based adapter number.

### -field netnum

IPX network number for the associated adapter.

### -field nodenum

IPX node address for the associated adapter.

### -field wan

Specifies whether the adapter is on a wide area network (WAN) link. When <b>TRUE</b>, the adapter is on a WAN link.

### -field status

Specifies whether the WAN link is up. <b>FALSE</b> indicates that the WAN link is up or the adapter is not on a WAN. Compare with the <b>wan</b> member to determine the meaning.

### -field maxpkt

Maximum allowable packet size, excluding the IPX header.

### -field linkspeed

Link speed, returned in 100 byte-per-second increments. For example, a 9600 byte-per-second link would return a value of 96.

## -remarks

Adapter numbers are base zero, so if there are eight adapters on a given computer, they are numbered 0-7. To determine the number of adapters present on the computer, call the 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function with IPX_MAX_ADAPTER_NUM.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>