---
UID: NS:lmaccess._NETLOGON_INFO_2
title: NETLOGON_INFO_2 (lmaccess.h)
description: Defines a level-2 control query response from a domain controller.
helpviewer_keywords: ["*PNETLOGON_INFO_2","NETLOGON_DNS_UPDATE_FAILURE","NETLOGON_FULL_SYNC_REPLICATION","NETLOGON_HAS_IP","NETLOGON_HAS_TIMESERV","NETLOGON_INFO_2","NETLOGON_INFO_2 structure [Windows API]","NETLOGON_REDO_NEEDED","NETLOGON_REPLICATION_IN_PROGRESS","NETLOGON_REPLICATION_NEEDED","NETLOGON_VERIFY_STATUS_RETURNED","PNETLOGON_INFO_2","PNETLOGON_INFO_2 structure pointer [Windows API]","lmaccess/NETLOGON_INFO_2","lmaccess/PNETLOGON_INFO_2","winprog.netlogon_info_2"]
old-location: winprog\netlogon_info_2.htm
tech.root: winprog
ms.assetid: ab29013d-e93a-4f15-84e1-c0e3e55b288d
ms.date: 12/05/2018
ms.keywords: '*PNETLOGON_INFO_2, NETLOGON_DNS_UPDATE_FAILURE, NETLOGON_FULL_SYNC_REPLICATION, NETLOGON_HAS_IP, NETLOGON_HAS_TIMESERV, NETLOGON_INFO_2, NETLOGON_INFO_2 structure [Windows API], NETLOGON_REDO_NEEDED, NETLOGON_REPLICATION_IN_PROGRESS, NETLOGON_REPLICATION_NEEDED, NETLOGON_VERIFY_STATUS_RETURNED, PNETLOGON_INFO_2, PNETLOGON_INFO_2 structure pointer [Windows API], lmaccess/NETLOGON_INFO_2, lmaccess/PNETLOGON_INFO_2, winprog.netlogon_info_2'
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
req.typenames: NETLOGON_INFO_2, *PNETLOGON_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETLOGON_INFO_2
 - lmaccess/_NETLOGON_INFO_2
 - PNETLOGON_INFO_2
 - lmaccess/PNETLOGON_INFO_2
 - NETLOGON_INFO_2
 - lmaccess/NETLOGON_INFO_2
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
 - NETLOGON_INFO_2
---

# NETLOGON_INFO_2 structure


## -description

The <b>NETLOGON_INFO_2</b> structure defines a level-2 control query response from a domain controller.

## -struct-fields

### -field netlog2_flags

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
<tr>
<td width="40%"><a id="NETLOGON_VERIFY_STATUS_RETURNED"></a><a id="netlogon_verify_status_returned"></a><dl>
<dt><b>NETLOGON_VERIFY_STATUS_RETURNED</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Trust verification status was returned in the <b>netlog2_pdc_connection_status</b> member.

</td>
</tr>
</table>

### -field netlog2_pdc_connection_status

An enumerated integer value that contains a status code defined in Lmerr.h, with a value greater than 2100.   If <b>NETLOGON_VERIFY_STATUS_RETURNED</b> is set in <b>netlog2_flags</b>, this value represents the trust verification status of all domain members  collectively.

### -field netlog2_trusted_dc_name.string

### -field netlog2_trusted_dc_name

A marshaled pointer to a string that contains the name of the trusted domain controller.

### -field netlog2_tc_connection_status

An enumerated integer value that contains a status code defined in Lmerr.h, with a value greater than 2100. This code shows the status of the secure channel to the specified trusted DC.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-i_netlogoncontrol2">I_NetLogonControl2</a>