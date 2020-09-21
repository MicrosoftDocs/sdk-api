---
UID: NS:ntsecpkg._SECPKG_CALL_INFO
title: SECPKG_CALL_INFO (ntsecpkg.h)
description: Contains information about a currently executing call.
helpviewer_keywords: ["*PSECPKG_CALL_INFO","PSECPKG_CALL_INFO","PSECPKG_CALL_INFO structure pointer [Security]","SECPKG_CALL_ANSI","SECPKG_CALL_ASYNC_UPDATE","SECPKG_CALL_BUFFER_MARSHALL","SECPKG_CALL_CLEANUP","SECPKG_CALL_INFO","SECPKG_CALL_INFO structure [Security]","SECPKG_CALL_IN_PROC","SECPKG_CALL_IS_TCB","SECPKG_CALL_KERNEL_MODE","SECPKG_CALL_NEGO","SECPKG_CALL_NEGO_EXTENDER","SECPKG_CALL_NETWORK_ONLY","SECPKG_CALL_PROCESS_TERM","SECPKG_CALL_RECURSIVE","SECPKG_CALL_SYSTEM_PROC","SECPKG_CALL_THREAD_TERM","SECPKG_CALL_URGENT","SECPKG_CALL_WINLOGON","SECPKG_CALL_WOWCLIENT","_ssp_secpkg_call_info","ntsecpkg/PSECPKG_CALL_INFO","ntsecpkg/SECPKG_CALL_INFO","security.secpkg_call_info"]
old-location: security\secpkg_call_info.htm
tech.root: security
ms.assetid: ac25ef88-7c64-42dd-8daa-fad039453043
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_CALL_INFO, PSECPKG_CALL_INFO, PSECPKG_CALL_INFO structure pointer [Security], SECPKG_CALL_ANSI, SECPKG_CALL_ASYNC_UPDATE, SECPKG_CALL_BUFFER_MARSHALL, SECPKG_CALL_CLEANUP, SECPKG_CALL_INFO, SECPKG_CALL_INFO structure [Security], SECPKG_CALL_IN_PROC, SECPKG_CALL_IS_TCB, SECPKG_CALL_KERNEL_MODE, SECPKG_CALL_NEGO, SECPKG_CALL_NEGO_EXTENDER, SECPKG_CALL_NETWORK_ONLY, SECPKG_CALL_PROCESS_TERM, SECPKG_CALL_RECURSIVE, SECPKG_CALL_SYSTEM_PROC, SECPKG_CALL_THREAD_TERM, SECPKG_CALL_URGENT, SECPKG_CALL_WINLOGON, SECPKG_CALL_WOWCLIENT, _ssp_secpkg_call_info, ntsecpkg/PSECPKG_CALL_INFO, ntsecpkg/SECPKG_CALL_INFO, security.secpkg_call_info'
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SECPKG_CALL_INFO, *PSECPKG_CALL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_CALL_INFO
 - ntsecpkg/_SECPKG_CALL_INFO
 - PSECPKG_CALL_INFO
 - ntsecpkg/PSECPKG_CALL_INFO
 - SECPKG_CALL_INFO
 - ntsecpkg/SECPKG_CALL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_CALL_INFO
---

# SECPKG_CALL_INFO structure


## -description

The <b>SECPKG_CALL_INFO</b> structure contains information about a currently executing call. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_call_info">GetCallInfo</a> function.

## -struct-fields

### -field ProcessId

The process identifier of the call.

### -field ThreadId

The thread identifier of the call.

### -field Attributes

The set of attribute flags that describe the call. The following table lists the valid attribute flag values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_KERNEL_MODE"></a><a id="secpkg_call_kernel_mode"></a><dl>
<dt><b>SECPKG_CALL_KERNEL_MODE</b></dt>
</dl>
</td>
<td width="60%">
Call originated in kernel mode.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_ANSI"></a><a id="secpkg_call_ansi"></a><dl>
<dt><b>SECPKG_CALL_ANSI</b></dt>
</dl>
</td>
<td width="60%">
Call came from ANSI stub.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_URGENT"></a><a id="secpkg_call_urgent"></a><dl>
<dt><b>SECPKG_CALL_URGENT</b></dt>
</dl>
</td>
<td width="60%">
Call designated urgent.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_RECURSIVE"></a><a id="secpkg_call_recursive"></a><dl>
<dt><b>SECPKG_CALL_RECURSIVE</b></dt>
</dl>
</td>
<td width="60%">
Call is recursive.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_IN_PROC"></a><a id="secpkg_call_in_proc"></a><dl>
<dt><b>SECPKG_CALL_IN_PROC</b></dt>
</dl>
</td>
<td width="60%">
Call originated in process.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_CLEANUP"></a><a id="secpkg_call_cleanup"></a><dl>
<dt><b>SECPKG_CALL_CLEANUP</b></dt>
</dl>
</td>
<td width="60%">
Call is cleanup from a client.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_WOWCLIENT"></a><a id="secpkg_call_wowclient"></a><dl>
<dt><b>SECPKG_CALL_WOWCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Call is from a WOW client process.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_THREAD_TERM"></a><a id="secpkg_call_thread_term"></a><dl>
<dt><b>SECPKG_CALL_THREAD_TERM</b></dt>
</dl>
</td>
<td width="60%">
Call is from a terminated thread. 

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_PROCESS_TERM"></a><a id="secpkg_call_process_term"></a><dl>
<dt><b>SECPKG_CALL_PROCESS_TERM</b></dt>
</dl>
</td>
<td width="60%">
Call is from a terminated process.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_IS_TCB"></a><a id="secpkg_call_is_tcb"></a><dl>
<dt><b>SECPKG_CALL_IS_TCB</b></dt>
</dl>
</td>
<td width="60%">
Call is from TCB.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_NETWORK_ONLY"></a><a id="secpkg_call_network_only"></a><dl>
<dt><b>SECPKG_CALL_NETWORK_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Call asks for network logon only and not any cached logons.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_WINLOGON"></a><a id="secpkg_call_winlogon"></a><dl>
<dt><b>SECPKG_CALL_WINLOGON</b></dt>
</dl>
</td>
<td width="60%">
Call of <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> is from Winlogon.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_ASYNC_UPDATE"></a><a id="secpkg_call_async_update"></a><dl>
<dt><b>SECPKG_CALL_ASYNC_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Asynchronous update for unlock.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_SYSTEM_PROC"></a><a id="secpkg_call_system_proc"></a><dl>
<dt><b>SECPKG_CALL_SYSTEM_PROC</b></dt>
</dl>
</td>
<td width="60%">
Call originated from the System process.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_NEGO"></a><a id="secpkg_call_nego"></a><dl>
<dt><b>SECPKG_CALL_NEGO</b></dt>
</dl>
</td>
<td width="60%">
Call is from SPNego.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_NEGO_EXTENDER"></a><a id="secpkg_call_nego_extender"></a><dl>
<dt><b>SECPKG_CALL_NEGO_EXTENDER</b></dt>
</dl>
</td>
<td width="60%">
Call is from NEGO extender.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_CALL_BUFFER_MARSHALL"></a><a id="secpkg_call_buffer_marshall"></a><dl>
<dt><b>SECPKG_CALL_BUFFER_MARSHALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed is marshaled by RPC.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -field CallCount

The call count.

### -field MechOid