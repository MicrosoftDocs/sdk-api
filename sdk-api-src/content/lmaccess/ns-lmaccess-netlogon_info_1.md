---
UID: NS:lmaccess._NETLOGON_INFO_1
title: NETLOGON_INFO_1 (lmaccess.h)
description: Defines a level-1 control query response from a domain controller.
helpviewer_keywords: ["*PNETLOGON_INFO_1","NETLOGON_DNS_UPDATE_FAILURE","NETLOGON_FULL_SYNC_REPLICATION","NETLOGON_HAS_IP","NETLOGON_HAS_TIMESERV","NETLOGON_INFO_1","NETLOGON_INFO_1 structure [Windows API]","NETLOGON_REDO_NEEDED","NETLOGON_REPLICATION_IN_PROGRESS","NETLOGON_REPLICATION_NEEDED","PNETLOGON_INFO_1","PNETLOGON_INFO_1 structure pointer [Windows API]","lmaccess/NETLOGON_INFO_1","lmaccess/PNETLOGON_INFO_1","winprog.netlogon_info_1"]
old-location: winprog\netlogon_info_1.htm
tech.root: winprog
ms.assetid: 053e937a-c7a9-4b8f-9312-32c82b705c08
ms.date: 12/05/2018
ms.keywords: '*PNETLOGON_INFO_1, NETLOGON_DNS_UPDATE_FAILURE, NETLOGON_FULL_SYNC_REPLICATION, NETLOGON_HAS_IP, NETLOGON_HAS_TIMESERV, NETLOGON_INFO_1, NETLOGON_INFO_1 structure [Windows API], NETLOGON_REDO_NEEDED, NETLOGON_REPLICATION_IN_PROGRESS, NETLOGON_REPLICATION_NEEDED, PNETLOGON_INFO_1, PNETLOGON_INFO_1 structure pointer [Windows API], lmaccess/NETLOGON_INFO_1, lmaccess/PNETLOGON_INFO_1, winprog.netlogon_info_1'
f1_keywords:
- lmaccess/NETLOGON_INFO_1
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Lmaccess.h
api_name:
- NETLOGON_INFO_1
targetos: Windows
req.typenames: NETLOGON_INFO_1, *PNETLOGON_INFO_1
req.redist: 
ms.custom: 19H1
---

# NETLOGON_INFO_1 structure


## -description


The <b>NETLOGON_INFO_1</b> structure defines a level-1 control query response from a domain controller.


## -struct-fields




### -field netlog1_flags

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
 


### -field netlog1_pdc_connection_status

An enumerated integer value that contains a status code defined in Lmerr.h, with a value greater than 2100.  This value applies only to backup domain controllers, and shows the status of the secure channel connection to the PDC in their domain.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmaccess/nf-lmaccess-i_netlogoncontrol2">I_NetLogonControl2</a>
 

 

