---
UID: NS:lmserver._SERVER_INFO_503
title: SERVER_INFO_503 (lmserver.h)
description: The SERVER_INFO_503 structure is obsolete. The structure contains information about the specified server.
helpviewer_keywords: ["*LPSERVER_INFO_503","*PSERVER_INFO_503","LPSERVER_INFO_503","LPSERVER_INFO_503 structure pointer [Network Management]","PSERVER_INFO_503","PSERVER_INFO_503 structure pointer [Network Management]","SERVER_INFO_503","SERVER_INFO_503 structure [Network Management]","_win32_server_info_503_str","lmserver/LPSERVER_INFO_503","lmserver/PSERVER_INFO_503","lmserver/SERVER_INFO_503","netmgmt.server_info_503_str"]
old-location: netmgmt\server_info_503_str.htm
tech.root: NetMgmt
ms.assetid: c6ad20ed-9f2b-4cbe-ac2e-a57acf1b32ea
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_503, *PSERVER_INFO_503, LPSERVER_INFO_503, LPSERVER_INFO_503 structure pointer [Network Management], PSERVER_INFO_503, PSERVER_INFO_503 structure pointer [Network Management], SERVER_INFO_503, SERVER_INFO_503 structure [Network Management], _win32_server_info_503_str, lmserver/LPSERVER_INFO_503, lmserver/PSERVER_INFO_503, lmserver/SERVER_INFO_503, netmgmt.server_info_503_str'
req.header: lmserver.h
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
req.typenames: SERVER_INFO_503, *PSERVER_INFO_503, *LPSERVER_INFO_503
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_503
 - lmserver/_SERVER_INFO_503
 - PSERVER_INFO_503
 - lmserver/PSERVER_INFO_503
 - SERVER_INFO_503
 - lmserver/SERVER_INFO_503
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_503
---

# SERVER_INFO_503 structure


## -description

The
				<b>SERVER_INFO_503</b> structure is obsolete. The structure contains information about the specified server.

## -struct-fields

### -field sv503_sessopens

Type: <b>DWORD</b>

The number of files that can be open in one session.

### -field sv503_sessvcs

Type: <b>DWORD</b>

The maximum number of sessions or virtual circuits permitted per client.

### -field sv503_opensearch

Type: <b>DWORD</b>

The number of search operations that can be carried out simultaneously.

### -field sv503_sizreqbuf

Type: <b>DWORD</b>

The size, in bytes, of each server buffer.

### -field sv503_initworkitems

Type: <b>DWORD</b>

The initial number of receive buffers, or work items, used by the server.

### -field sv503_maxworkitems

Type: <b>DWORD</b>

The maximum number of receive buffers, or work items, the server can allocate. If this limit is reached, the transport must initiate flow control at a significant performance cost.

### -field sv503_rawworkitems

Type: <b>DWORD</b>

The number of special work items the server uses for raw mode I/O. A larger value for this member can increase performance but it requires more memory.

### -field sv503_irpstacksize

Type: <b>DWORD</b>

The number of stack locations that the server allocated in I/O request packets (IRPs).

### -field sv503_maxrawbuflen

Type: <b>DWORD</b>

The maximum raw mode buffer size, in bytes.

### -field sv503_sessusers

Type: <b>DWORD</b>

The maximum number of users that can be logged on to the server using a single session or virtual circuit.

### -field sv503_sessconns

Type: <b>DWORD</b>

The maximum number of tree connections that can be made on the server using a single session or virtual circuit.

### -field sv503_maxpagedmemoryusage

Type: <b>DWORD</b>

The maximum size, in bytes, of pageable memory that the server can allocate at any one time.

### -field sv503_maxnonpagedmemoryusage

### -field sv503_enablesoftcompat

Type: <b>BOOL</b>

A value that indicates whether the server maps a request to a normal open request with shared-read access when the server receives a compatibility open request with read access. Mapping such requests allows several MS-DOS computers to open a single file for read access. This member is unused.

### -field sv503_enableforcedlogoff

Type: <b>BOOL</b>

A value that indicates whether the server should force a client to disconnect, even if the client has open files, once the client's logon time has expired.

### -field sv503_timesource

Type: <b>BOOL</b>

A value that indicates whether the server is a reliable time source.

### -field sv503_acceptdownlevelapis

Type: <b>BOOL</b>

A value that indicates whether the server accepts function calls from previous-generation LAN Manager clients.

### -field sv503_lmannounce

Type: <b>BOOL</b>

A value that indicates whether the server is visible to LAN Manager 2.x clients.

### -field sv503_domain

Type: <b>LPWSTR</b>

A pointer to a Unicode character string that specifies the name of the server's domain.

### -field sv503_maxcopyreadlen

Type: <b>DWORD</b>

The maximum length, in bytes, of copy reads on the server.

This member is unused.

### -field sv503_maxcopywritelen

Type: <b>DWORD</b>

The maximum length, in bytes, of copy writes on the server.

This member is unused.

### -field sv503_minkeepsearch

Type: <b>DWORD</b>

The minimum length of time the server retains information about incomplete search operations. This member is unused.

### -field sv503_maxkeepsearch

Type: <b>DWORD</b>

The maximum length of time, in seconds,  the server retains information about incomplete search operations.

### -field sv503_minkeepcomplsearch

Type: <b>DWORD</b>

The minimum length of time, in seconds, the server retains information about complete search operations. This member is unused.

### -field sv503_maxkeepcomplsearch

Type: <b>DWORD</b>

The maximum length of time, in seconds, the server retains information about complete search operations. This member is unused.

### -field sv503_threadcountadd

Type: <b>DWORD</b>

The number of additional threads the server should use in addition to one worker thread per processor it already uses. This member is unused.

### -field sv503_numblockthreads

Type: <b>DWORD</b>

The number of threads set aside by the server to service requests that can block the thread for a significant amount of time.  This member is unused.

### -field sv503_scavtimeout

Type: <b>DWORD</b>

The period of time, in seconds, that the scavenger remains idle before waking up to service requests.

### -field sv503_minrcvqueue

Type: <b>DWORD</b>

The minimum number of free receive work items the server requires before it begins to allocate more.

### -field sv503_minfreeworkitems

Type: <b>DWORD</b>

The minimum number of available receive work items that the server requires to begin processing a server message block.

### -field sv503_xactmemsize

Type: <b>DWORD</b>

The size, in bytes, of the shared memory region used to process server functions.

### -field sv503_threadpriority

Type: <b>DWORD</b>

The priority of all server threads in relation to the base priority of the process.

### -field sv503_maxmpxct

Type: <b>DWORD</b>

The maximum number of outstanding requests that any one client can send to the server. For example, 10 means you can have 10 unanswered requests at the server. When any single client has 10 requests queued within the server, the client must wait for a server response before sending another request.

### -field sv503_oplockbreakwait

Type: <b>DWORD</b>

The period of time, in seconds, to wait before timing out an opportunistic lock break request.

### -field sv503_oplockbreakresponsewait

Type: <b>DWORD</b>

The period of time, in seconds, the server waits for a client to respond to an oplock break request from the server.

### -field sv503_enableoplocks

Type: <b>BOOL</b>

A value that indicates whether the server allows clients to use opportunistic locks on files. Opportunistic locks are a significant performance enhancement, but have the potential to cause lost cached data on some networks, particularly wide-area networks.

### -field sv503_enableoplockforceclose

Type: <b>BOOL</b>

A value that indicates how the server should behave if a client has an opportunistic lock (oplock) and does not respond to an oplock break. This member indicates whether the server will fail the second open (value of 0), or force close the open instance of a client that has an oplock (value equal to 1). This member is unused.

### -field sv503_enablefcbopens

Type: <b>BOOL</b>

A value that indicates whether several MS-DOS File Control Blocks (FCBs) are placed in a single location accessible to the server. If enabled, this can save resources on the server.

### -field sv503_enableraw

Type: <b>BOOL</b>

A value that indicates whether the server processes raw Server Message Blocks (SMBs). If enabled, this allows more data to transfer per transaction and also improves performance. However, it is possible that processing raw SMBs can impede performance on certain networks. The server maintains the value of this member.

### -field sv503_enablesharednetdrives

Type: <b>BOOL</b>

A value that indicates whether the server allows redirected server drives to be shared.

### -field sv503_minfreeconnections

Type: <b>DWORD</b>

The minimum number of free connection blocks maintained per endpoint. The server sets these aside to handle bursts of requests by clients to connect to the server.

### -field sv503_maxfreeconnections

Type: <b>DWORD</b>

The maximum number of free connection blocks maintained per endpoint. The server sets these aside to    handle bursts of requests by clients to connect to the server.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>