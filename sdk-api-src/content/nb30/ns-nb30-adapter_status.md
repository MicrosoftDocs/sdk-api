---
UID: NS:nb30._ADAPTER_STATUS
title: ADAPTER_STATUS (nb30.h)
description: The ADAPTER_STATUS structure contains information about a network adapter.
helpviewer_keywords: ["*PADAPTER_STATUS","ADAPTER_STATUS","ADAPTER_STATUS structure [NetBIOS]","PADAPTER_STATUS","PADAPTER_STATUS structure pointer [NetBIOS]","nb30/ADAPTER_STATUS","nb30/PADAPTER_STATUS","netbios.adapter_status"]
old-location: netbios\adapter_status.htm
tech.root: NetBIOS
ms.assetid: 402bc5ce-bce4-4ba9-b82d-13cd3dc7097b
ms.date: 12/05/2018
ms.keywords: '*PADAPTER_STATUS, ADAPTER_STATUS, ADAPTER_STATUS structure [NetBIOS], PADAPTER_STATUS, PADAPTER_STATUS structure pointer [NetBIOS], nb30/ADAPTER_STATUS, nb30/PADAPTER_STATUS, netbios.adapter_status'
req.header: nb30.h
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
req.typenames: ADAPTER_STATUS, *PADAPTER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADAPTER_STATUS
 - nb30/_ADAPTER_STATUS
 - PADAPTER_STATUS
 - nb30/PADAPTER_STATUS
 - ADAPTER_STATUS
 - nb30/ADAPTER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - ADAPTER_STATUS
---

# ADAPTER_STATUS structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>ADAPTER_STATUS</b> structure contains information about a network adapter. This structure is pointed to by the <b>ncb_buffer</b> member of the <a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure. <b>ADAPTER_STATUS</b> is followed by as many <a href="/windows/desktop/api/nb30/ns-nb30-name_buffer">NAME_BUFFER</a> structures as required to describe the network adapters on the system.

## -struct-fields

### -field adapter_address

Specifies encoded address of the adapter.

### -field rev_major

Specifies the major software-release level. This value is 3 for IBM NetBIOS 3. x.

### -field reserved0

Reserved. This value is always zero.

### -field adapter_type

Specifies the adapter type. This value is 0xFF for a Token Ring adapter or 0xFE for an Ethernet adapter.

### -field rev_minor

Specifies the minor software-release level. This value is zero for IBM NetBIOS x.0.

### -field duration

Specifies the duration of the reporting period, in minutes.

### -field frmr_recv

Specifies the number of FRMR frames received.

### -field frmr_xmit

Specifies the number of FRMR frames transmitted.

### -field iframe_recv_err

Specifies the number of I frames received in error.

### -field xmit_aborts

Specifies the number of aborted transmissions.

### -field xmit_success

Specifies the number of successfully transmitted packets.

### -field recv_success

Specifies the number of successfully received packets.

### -field iframe_xmit_err

Specifies the number of I frames transmitted in error.

### -field recv_buff_unavail

Specifies the number of times a buffer was not available to service a request from a remote computer.

### -field t1_timeouts

Specifies the number of times that the DLC T1 timer timed out.

<b>Windows 95:  </b>DLC is no longer supported.

### -field ti_timeouts

Specifies the number of times that the ti inactivity timer timed out. The ti timer is used to detect links that have been broken.

### -field reserved1

Reserved. This value is always zero.

### -field free_ncbs

Specifies the current number of free network control blocks.

### -field max_cfg_ncbs

Undefined for IBM NetBIOS 3.0.

### -field max_ncbs

Undefined for IBM NetBIOS 3.0.

### -field xmit_buf_unavail

Undefined for IBM NetBIOS 3.0.

### -field max_dgram_size

Specifies the maximum size of a datagram packet. This value is always at least 512 bytes.

### -field pending_sess

Specifies the number of pending sessions.

### -field max_cfg_sess

Specifies the configured maximum pending sessions.

### -field max_sess

Undefined for IBM NetBIOS 3.0.

### -field max_sess_pkt_size

Specifies the maximum size of a session data packet.

### -field name_count

Specifies the number of names in the local names table.

## -see-also

<b></b>



<a href="/windows/desktop/api/nb30/ns-nb30-name_buffer">NAME_BUFFER</a>



<a href="/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>