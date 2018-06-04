---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _NETLOGON_INFO_3 structure


## -description


The <b>NETLOGON_INFO_3</b> structure defines a level-3 control query response from a domain controller.


## -struct-fields




### -field netlog3_flags

 


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


#### - netlog1_flags

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
 


## -see-also




<a href="https://msdn.microsoft.com/bf40ee60-3a13-4a4e-a0f4-ba7c9fc11097">I_NetLogonControl2</a>
 

 

