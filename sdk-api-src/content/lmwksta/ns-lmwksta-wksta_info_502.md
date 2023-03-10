---
UID: NS:lmwksta._WKSTA_INFO_502
title: WKSTA_INFO_502 (lmwksta.h)
description: The WKSTA_INFO_502 structure is obsolete. The structure contains information about a workstation environment.
helpviewer_keywords: ["*LPWKSTA_INFO_502","*PWKSTA_INFO_502","LPWKSTA_INFO_502","LPWKSTA_INFO_502 structure pointer [Network Management]","PWKSTA_INFO_502","PWKSTA_INFO_502 structure pointer [Network Management]","WKSTA_INFO_502","WKSTA_INFO_502 structure [Network Management]","_win32_wksta_info_502_str","lmwksta/LPWKSTA_INFO_502","lmwksta/PWKSTA_INFO_502","lmwksta/WKSTA_INFO_502","netmgmt.wksta_info_502_str"]
old-location: netmgmt\wksta_info_502_str.htm
tech.root: NetMgmt
ms.assetid: 716e700a-e464-47ec-a2df-74c03597ac6d
ms.date: 12/05/2018
ms.keywords: '*LPWKSTA_INFO_502, *PWKSTA_INFO_502, LPWKSTA_INFO_502, LPWKSTA_INFO_502 structure pointer [Network Management], PWKSTA_INFO_502, PWKSTA_INFO_502 structure pointer [Network Management], WKSTA_INFO_502, WKSTA_INFO_502 structure [Network Management], _win32_wksta_info_502_str, lmwksta/LPWKSTA_INFO_502, lmwksta/PWKSTA_INFO_502, lmwksta/WKSTA_INFO_502, netmgmt.wksta_info_502_str'
req.header: lmwksta.h
req.include-header: Lm.h
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
req.typenames: WKSTA_INFO_502, *PWKSTA_INFO_502, *LPWKSTA_INFO_502
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WKSTA_INFO_502
 - lmwksta/_WKSTA_INFO_502
 - PWKSTA_INFO_502
 - lmwksta/PWKSTA_INFO_502
 - WKSTA_INFO_502
 - lmwksta/WKSTA_INFO_502
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_INFO_502
---

# WKSTA_INFO_502 structure


## -description

The
				<b>WKSTA_INFO_502</b> structure is obsolete. The structure contains information about a workstation environment.

## -struct-fields

### -field wki502_char_wait

Type: <b>DWORD</b>

The number of seconds the computer waits for a remote resource to become available.

### -field wki502_collection_time

Type: <b>DWORD</b>

The number of milliseconds the computer collects data before sending the data to a character device resource. The workstation waits the specified time or collects the number of characters specified by the <b>wki502_maximum_collection_count</b>  member, whichever comes first.

### -field wki502_maximum_collection_count

Type: <b>DWORD</b>

The number of bytes of information the computer collects before sending the data to a character device resource. The workstation collects the specified number of bytes or waits the period of time specified by the <b>wki502_collection_time</b>  member, whichever comes first.

### -field wki502_keep_conn

Type: <b>DWORD</b>

The number of seconds the server maintains an inactive connection to a server's resource.

### -field wki502_max_cmds

Type: <b>DWORD</b>

The number of simultaneous network device driver commands that can be sent to the network.

### -field wki502_sess_timeout

Type: <b>DWORD</b>

The number of seconds the server waits before disconnecting an inactive session.

### -field wki502_siz_char_buf

Type: <b>DWORD</b>

The maximum size, in bytes, of a character pipe buffer and device buffer.

### -field wki502_max_threads

Type: <b>DWORD</b>

The number of threads the computer can dedicate to the network.

### -field wki502_lock_quota

Type: <b>DWORD</b>

Reserved.

### -field wki502_lock_increment

Type: <b>DWORD</b>

Reserved.

### -field wki502_lock_maximum

Type: <b>DWORD</b>

Reserved.

### -field wki502_pipe_increment

Type: <b>DWORD</b>

Reserved.

### -field wki502_pipe_maximum

Type: <b>DWORD</b>

Reserved.

### -field wki502_cache_file_timeout

Type: <b>DWORD</b>

Reserved.

### -field wki502_dormant_file_limit

Type: <b>DWORD</b>

Reserved.

### -field wki502_read_ahead_throughput

Type: <b>DWORD</b>

Reserved.

### -field wki502_num_mailslot_buffers

Type: <b>DWORD</b>

Reserved.

### -field wki502_num_srv_announce_buffers

Type: <b>DWORD</b>

Reserved.

### -field wki502_max_illegal_datagram_events

Type: <b>DWORD</b>

Reserved.

### -field wki502_illegal_datagram_event_reset_frequency

Type: <b>DWORD</b>

Reserved.

### -field wki502_log_election_packets

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_opportunistic_locking

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_unlock_behind

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_close_behind

Type: <b>BOOL</b>

Reserved.

### -field wki502_buf_named_pipes

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_lock_read_unlock

Type: <b>BOOL</b>

Reserved.

### -field wki502_utilize_nt_caching

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_raw_read

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_raw_write

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_write_raw_data

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_encryption

Type: <b>BOOL</b>

Reserved.

### -field wki502_buf_files_deny_write

Type: <b>BOOL</b>

Reserved.

### -field wki502_buf_read_only_files

Type: <b>BOOL</b>

Reserved.

### -field wki502_force_core_create_mode

Type: <b>BOOL</b>

Reserved.

### -field wki502_use_512_byte_max_transfer

Type: <b>BOOL</b>

Reserved.

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstagetinfo">NetWkstaGetInfo</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstasetinfo">NetWkstaSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>