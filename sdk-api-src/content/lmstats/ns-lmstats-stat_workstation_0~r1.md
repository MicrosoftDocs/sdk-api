---
UID: NS:lmstats._STAT_WORKSTATION_0~r1
title: STAT_WORKSTATION_0
description: The STAT_WORKSTATION_0 structure (lmstats.h) contains statistical information about the specified workstation.
ms.date: 02/14/2023
ms.keywords: _STAT_WORKSTATION_0, STAT_WORKSTATION_0
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: lmstats.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: STAT_WORKSTATION_0, *PSTAT_WORKSTATION_0, *LPSTAT_WORKSTATION_0
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _STAT_WORKSTATION_0
 - lmstats/_STAT_WORKSTATION_0
 - PSTAT_WORKSTATION_0
 - lmstats/PSTAT_WORKSTATION_0
 - STAT_WORKSTATION_0
 - lmstats/STAT_WORKSTATION_0
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - lmstats.h
api_name:
 - _STAT_WORKSTATION_0
 - STAT_WORKSTATION_0
---

# STAT_WORKSTATION_0 structure

## -description

Contains statistical information about the specified workstation.

## -struct-fields

### -field StatisticsStartTime

Specifies the time statistics collection started.

This member also indicates when statistics for the workstations were last cleared. The value is stored as the number of seconds elapsed since 00:00:00, January 1, 1970.

### -field BytesReceived

Specifies the total number of bytes received by the workstation.

### -field SmbsReceived

Specifies the total number of server message blocks (SMBs) received by the workstation.

### -field PagingReadBytesRequested

Specifies the total number of bytes that have been read by paging I/O requests.

### -field NonPagingReadBytesRequested

Specifies the total number of bytes that have been read by non-paging I/O requests.

### -field CacheReadBytesRequested

Specifies the total number of bytes that have been read by cache I/O requests.

### -field NetworkReadBytesRequested

Specifies the total amount of bytes that have been read by disk I/O requests.

### -field BytesTransmitted

Specifies the total number of bytes transmitted by the workstation.

### -field SmbsTransmitted

Specifies the total number of SMBs transmitted by the workstation.

### -field PagingWriteBytesRequested

Specifies the total number of bytes that have been written by paging I/O requests.

### -field NonPagingWriteBytesRequested

Specifies the total number of bytes that have been written by non-paging I/O requests.

### -field CacheWriteBytesRequested

Specifies the total number of bytes that have been written by cache I/O requests.

### -field NetworkWriteBytesRequested

Specifies the total number of bytes that have been written by disk I/O requests.

### -field InitiallyFailedOperations

Specifies the total number of network operations that failed to begin.

### -field FailedCompletionOperations

Specifies the total number of network operations that failed to complete.

### -field ReadOperations

Specifies the total number of read operations initiated by the workstation.

### -field RandomReadOperations

Specifies the total number of random access reads initiated by the workstation.

### -field ReadSmbs

Specifies the total number of read requests the workstation has sent to servers.

### -field LargeReadSmbs

Specifies the total number of read requests the workstation has sent to servers that are greater than twice the size of the server's negotiated buffer size.

### -field SmallReadSmbs

Specifies the total number of read requests the workstation has sent to servers that are less than 1/4 of the size of the server's negotiated buffer size.

### -field WriteOperations

Specifies the total number of write operations initiated by the workstation.

### -field RandomWriteOperations

Specifies the total number of random access writes initiated by the workstation.

### -field WriteSmbs

Specifies the total number of write requests the workstation has sent to servers.

### -field LargeWriteSmbs

Specifies the total number of write requests the workstation has sent to servers that are greater than twice the size of the server's negotiated buffer size.

### -field SmallWriteSmbs

Specifies the total number of write requests the workstation has sent to servers that are less than 1/4 of the size of the server's negotiated buffer size.

### -field RawReadsDenied

Specifies the total number of raw read requests made by the workstation that have been denied.

### -field RawWritesDenied

Specifies the total number of raw write requests made by the workstation that have been denied.

### -field NetworkErrors

Specifies the total number of network errors received by the workstation.

### -field Sessions

Specifies the total number of sessions established by the workstation.

### -field FailedSessions

Specifies the number of times the workstation attempted to create a session but failed.

### -field Reconnects

Specifies the total number of connections that have failed.

### -field CoreConnects

Specifies the total number of connections to servers supporting the PCNET dialect that have succeeded.

### -field Lanman20Connects

Specifies the total number of connections to servers supporting the LanManager 2.0 dialect that have succeeded.

### -field Lanman21Connects

Specifies the total number of connections to servers supporting the LanManager 2.1 dialect that have succeeded.

### -field LanmanNtConnects

Specifies the total number of connections to servers supporting the NTLM dialect that have succeeded.

### -field ServerDisconnects

Specifies the number of times the workstation was disconnected by a network server.

### -field HungSessions

Specifies the total number of sessions that have expired on the workstation.

### -field UseCount

Specifies the total number of network connections established by the workstation.

### -field FailedUseCount

Specifies the total number of failed network connections for the workstation.

### -field CurrentCommands

Specifies the number of current requests that have not been completed.

## -see-also

[NetStatisticsGet](/windows/win32/api/lmstats/nf-lmstats-netstatisticsget)

[Network Management Overview](/windows/win32/NetMgmt/network-management)

[Network Management Structures](/windows/win32/NetMgmt/network-management-structures)

[Statistics Functions](/windows/win32/NetShare/statistics-functions)
