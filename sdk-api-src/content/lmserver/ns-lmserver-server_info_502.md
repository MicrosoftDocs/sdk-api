---
UID: NS:lmserver._SERVER_INFO_502
title: SERVER_INFO_502 (lmserver.h)
description: The SERVER_INFO_502 structure is obsolete. The structure contains information about a specified server.
helpviewer_keywords: ["*LPSERVER_INFO_502","*PSERVER_INFO_502","LPSERVER_INFO_502","LPSERVER_INFO_502 structure pointer [Network Management]","PSERVER_INFO_502","PSERVER_INFO_502 structure pointer [Network Management]","SERVER_INFO_502","SERVER_INFO_502 structure [Network Management]","_win32_server_info_502_str","lmserver/LPSERVER_INFO_502","lmserver/PSERVER_INFO_502","lmserver/SERVER_INFO_502","netmgmt.server_info_502_str"]
old-location: netmgmt\server_info_502_str.htm
tech.root: NetMgmt
ms.assetid: 97657dff-7bd1-4108-934b-8203f41b3742
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_502, *PSERVER_INFO_502, LPSERVER_INFO_502, LPSERVER_INFO_502 structure pointer [Network Management], PSERVER_INFO_502, PSERVER_INFO_502 structure pointer [Network Management], SERVER_INFO_502, SERVER_INFO_502 structure [Network Management], _win32_server_info_502_str, lmserver/LPSERVER_INFO_502, lmserver/PSERVER_INFO_502, lmserver/SERVER_INFO_502, netmgmt.server_info_502_str'
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
req.typenames: SERVER_INFO_502, *PSERVER_INFO_502, *LPSERVER_INFO_502
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_502
 - lmserver/_SERVER_INFO_502
 - PSERVER_INFO_502
 - lmserver/PSERVER_INFO_502
 - SERVER_INFO_502
 - lmserver/SERVER_INFO_502
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
 - SERVER_INFO_502
---

# SERVER_INFO_502 structure


## -description

The
				<b>SERVER_INFO_502</b> structure is obsolete. The structure contains information about a specified server.

## -struct-fields

### -field sv502_sessopens

Type: <b>DWORD</b>

The number of files that can be open in one session.

### -field sv502_sessvcs

Type: <b>DWORD</b>

T he maximum number of virtual circuits permitted per client.

### -field sv502_opensearch

Type: <b>DWORD</b>

The number of search operations that can be carried out simultaneously.

### -field sv502_sizreqbuf

Type: <b>DWORD</b>

The size, in bytes, of each server buffer.

### -field sv502_initworkitems

Type: <b>DWORD</b>

The initial number of receive buffers, or work items, used by the server.

### -field sv502_maxworkitems

Type: <b>DWORD</b>

The maximum number of receive buffers, or work items, the server can allocate. If this limit is reached, the transport must initiate flow control at a significant performance cost.

### -field sv502_rawworkitems

Type: <b>DWORD</b>

The number of special work items the server uses for raw mode I/O. A large value for this member can increase performance, but it requires more memory.

### -field sv502_irpstacksize

Type: <b>DWORD</b>

The number of stack locations that the server allocated in I/O request packets (IRPs).

### -field sv502_maxrawbuflen

Type: <b>DWORD</b>

The maximum raw mode buffer size, in bytes.

### -field sv502_sessusers

Type: <b>DWORD</b>

The maximum number of users that can be logged on to the server using a single virtual circuit.

### -field sv502_sessconns

Type: <b>DWORD</b>

The maximum number of tree connections that can be made on the server using a single virtual circuit.

### -field sv502_maxpagedmemoryusage

Type: <b>DWORD</b>

The maximum size, in bytes, of pageable memory that the server can allocate at any one time.

### -field sv502_maxnonpagedmemoryusage

Type: <b>DWORD</b>

The maximum size, in bytes, of nonpaged memory that the server can allocate at any one time.

### -field sv502_enablesoftcompat

Type: <b>BOOL</b>

A value that indicates whether the server maps a request to a normal open request with shared-read access when the server receives a compatibility open request with read access. Mapping such requests allows several MS-DOS computers to open a single file for read access.

### -field sv502_enableforcedlogoff

Type: <b>BOOL</b>

A value that indicates whether the server should force a client to disconnect, even if the client has open files, once the client's logon time has expired.

### -field sv502_timesource

Type: <b>BOOL</b>

A value that indicates whether the server is a reliable time source.

### -field sv502_acceptdownlevelapis

Type: <b>BOOL</b>

A value that indicates whether the server accepts function calls from previous-generation LAN Manager clients.

### -field sv502_lmannounce

Type: <b>BOOL</b>

A value that indicates whether the server is visible to LAN Manager 2.x clients.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netserversetinfo">NetServerSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>