---
UID: NS:lmaccess._NETLOGON_INFO_3
title: NETLOGON_INFO_3 (lmaccess.h)
description: Defines a level-3 control query response from a domain controller.
helpviewer_keywords: ["*PNETLOGON_INFO_3","NETLOGON_DNS_UPDATE_FAILURE","NETLOGON_FULL_SYNC_REPLICATION","NETLOGON_HAS_IP","NETLOGON_HAS_TIMESERV","NETLOGON_INFO_3","NETLOGON_INFO_3 structure [Windows API]","NETLOGON_REDO_NEEDED","NETLOGON_REPLICATION_IN_PROGRESS","NETLOGON_REPLICATION_NEEDED","PNETLOGON_INFO_3","PNETLOGON_INFO_3 structure pointer [Windows API]","lmaccess/NETLOGON_INFO_3","lmaccess/PNETLOGON_INFO_3","winprog.netlogon_info_3"]
old-location: winprog\netlogon_info_3.htm
tech.root: winprog
ms.assetid: 6498c4b2-523a-4050-acbd-5088b9e0eaae
ms.date: 12/05/2018
ms.keywords: '*PNETLOGON_INFO_3, NETLOGON_DNS_UPDATE_FAILURE, NETLOGON_FULL_SYNC_REPLICATION, NETLOGON_HAS_IP, NETLOGON_HAS_TIMESERV, NETLOGON_INFO_3, NETLOGON_INFO_3 structure [Windows API], NETLOGON_REDO_NEEDED, NETLOGON_REPLICATION_IN_PROGRESS, NETLOGON_REPLICATION_NEEDED, PNETLOGON_INFO_3, PNETLOGON_INFO_3 structure pointer [Windows API], lmaccess/NETLOGON_INFO_3, lmaccess/PNETLOGON_INFO_3, winprog.netlogon_info_3'
req.header: lmaccess.h
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
req.typenames: NETLOGON_INFO_3, *PNETLOGON_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETLOGON_INFO_3
 - lmaccess/_NETLOGON_INFO_3
 - PNETLOGON_INFO_3
 - lmaccess/PNETLOGON_INFO_3
 - NETLOGON_INFO_3
 - lmaccess/NETLOGON_INFO_3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - NETLOGON_INFO_3
---

## -description

The <b>NETLOGON_INFO_3</b> structure defines a level-3 control query response from a domain controller.

## -struct-fields

### -field netlog3_flags

An integer value that contains one or more of the following control query responses from the DC.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_REPLICATION_NEEDED"></a><a id="netlogon_replication_needed"></a><dl>
<dt><b>NETLOGON_REPLICATION_NEEDED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Not supported. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_REPLICATION_IN_PROGRESS"></a><a id="netlogon_replication_in_progress"></a><dl>
<dt><b>NETLOGON_REPLICATION_IN_PROGRESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Not supported. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_FULL_SYNC_REPLICATION"></a><a id="netlogon_full_sync_replication"></a><dl>
<dt><b>NETLOGON_FULL_SYNC_REPLICATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Not supported. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_REDO_NEEDED"></a><a id="netlogon_redo_needed"></a><dl>
<dt><b>NETLOGON_REDO_NEEDED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Not supported. 

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_HAS_IP"></a><a id="netlogon_has_ip"></a><dl>
<dt><b>NETLOGON_HAS_IP</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Trusted domain DC has an IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_HAS_TIMESERV"></a><a id="netlogon_has_timeserv"></a><dl>
<dt><b>NETLOGON_HAS_TIMESERV</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Trusted domain DC runs the Windows Time Service.

</td>
</tr>
<tr>
<td width="40%"><a id="NETLOGON_DNS_UPDATE_FAILURE"></a><a id="netlogon_dns_update_failure"></a><dl>
<dt><b>NETLOGON_DNS_UPDATE_FAILURE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Last update to the DNS records on the DC failed.

</td>
</tr>
</table>

### -field netlog3_logon_attempts

The number of logon attempts made for the domain.

### -field netlog3_reserved1

Reserved value.

### -field netlog3_reserved2

Reserved value.

### -field netlog3_reserved3

Reserved value.

### -field netlog3_reserved4

Reserved value.

### -field netlog3_reserved5

Reserved value.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-i_netlogoncontrol2">I_NetLogonControl2</a>
