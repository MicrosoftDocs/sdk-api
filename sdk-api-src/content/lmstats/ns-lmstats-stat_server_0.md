---
UID: NS:lmstats._STAT_SERVER_0
title: STAT_SERVER_0 (lmstats.h)
description: Contains statistical information about the server.
helpviewer_keywords: ["*LPSTAT_SERVER_0","*PSTAT_SERVER_0","LPSTAT_SERVER_0","LPSTAT_SERVER_0 structure pointer [Files]","PSTAT_SERVER_0","PSTAT_SERVER_0 structure pointer [Files]","STAT_SERVER_0","STAT_SERVER_0 structure [Files]","_win32_stat_server_0_str","fs.stat_server_0_str","lmstats/LPSTAT_SERVER_0","lmstats/PSTAT_SERVER_0","lmstats/STAT_SERVER_0","netmgmt.stat_server_0_str"]
old-location: fs\stat_server_0_str.htm
tech.root: fs
ms.assetid: 7eb4e4a9-f4db-4702-a4ad-2d8bfac9f9ce
ms.date: 12/05/2018
ms.keywords: '*LPSTAT_SERVER_0, *PSTAT_SERVER_0, LPSTAT_SERVER_0, LPSTAT_SERVER_0 structure pointer [Files], PSTAT_SERVER_0, PSTAT_SERVER_0 structure pointer [Files], STAT_SERVER_0, STAT_SERVER_0 structure [Files], _win32_stat_server_0_str, fs.stat_server_0_str, lmstats/LPSTAT_SERVER_0, lmstats/PSTAT_SERVER_0, lmstats/STAT_SERVER_0, netmgmt.stat_server_0_str'
req.header: lmstats.h
req.include-header: Lm.h
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
req.typenames: STAT_SERVER_0, *PSTAT_SERVER_0, *LPSTAT_SERVER_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STAT_SERVER_0
 - lmstats/_STAT_SERVER_0
 - PSTAT_SERVER_0
 - lmstats/PSTAT_SERVER_0
 - STAT_SERVER_0
 - lmstats/STAT_SERVER_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmstats.h
api_name:
 - STAT_SERVER_0
---

# STAT_SERVER_0 structure


## -description

Contains statistical information about the server.

## -struct-fields

### -field sts0_start

Specifies a DWORD value that indicates the time when statistics collection started (or when the statistics were last cleared). The value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT. To calculate the length of time that statistics have been collected, subtract the value of this member from the present time.

### -field sts0_fopens

Specifies a DWORD value that indicates the number of times a file is opened on a server. This includes the number of times named pipes are opened.

### -field sts0_devopens

Specifies a DWORD value that indicates the number of times a server device is opened.

### -field sts0_jobsqueued

Specifies a DWORD value that indicates the number of server print jobs spooled.

### -field sts0_sopens

Specifies a DWORD value that indicates the number of times the server session started.

### -field sts0_stimedout

Specifies a DWORD value that indicates the number of times the server session automatically disconnected.

### -field sts0_serrorout

Specifies a DWORD value that indicates the number of times the server sessions failed with an error.

### -field sts0_pwerrors

Specifies a DWORD value that indicates the number of server password violations.

### -field sts0_permerrors

Specifies a DWORD value that indicates the number of server access permission errors.

### -field sts0_syserrors

Specifies a DWORD value that indicates the number of server system errors.

### -field sts0_bytessent_low

Specifies the low-order DWORD of the number of server bytes sent to the network.

### -field sts0_bytessent_high

Specifies the high-order DWORD of the number of server bytes sent to the network.

### -field sts0_bytesrcvd_low

Specifies the low-order DWORD of the number of server bytes received from the network.

### -field sts0_bytesrcvd_high

Specifies the high-order DWORD of the number of server bytes received from the network.

### -field sts0_avresponse

Specifies a DWORD value that indicates the average server response time (in milliseconds).

### -field sts0_reqbufneed

Specifies a DWORD value that indicates the number of times the server required a request buffer but failed to allocate one. This value indicates that the server parameters may need adjustment.

### -field sts0_bigbufneed

Specifies a DWORD value that indicates the number of times the server required a big buffer but failed to allocate one. This value indicates that the server parameters may need adjustment.

## -see-also

<a href="/windows/desktop/api/lmstats/nf-lmstats-netstatisticsget">NetStatisticsGet</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/statistics-functions">Statistics Functions</a>