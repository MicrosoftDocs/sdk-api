---
UID: NS:lmstats._STAT_WORKSTATION_0
title: "_STAT_WORKSTATION_0"
author: windows-driver-content
description: Contains statistical information about the specified workstation.
old-location: fs\stat_workstation_0_str.htm
old-project: NetShare
ms.assetid: 7a29fe54-fd15-499d-b255-f49025421861
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*LPSTAT_WORKSTATION_0, *PSTAT_WORKSTATION_0, LPSTAT_WORKSTATION_0, LPSTAT_WORKSTATION_0 structure pointer [Files], PSTAT_WORKSTATION_0, PSTAT_WORKSTATION_0 structure pointer [Files], STAT_WORKSTATION_0, STAT_WORKSTATION_0 structure [Files], _STAT_WORKSTATION_0, _win32_stat_workstation_0_str, fs.stat_workstation_0_str, lmstats/LPSTAT_WORKSTATION_0, lmstats/PSTAT_WORKSTATION_0, lmstats/STAT_WORKSTATION_0, netmgmt.stat_workstation_0_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: STAT_WORKSTATION_0, *PSTAT_WORKSTATION_0, *LPSTAT_WORKSTATION_0, STAT_WORKSTATION_0, *PSTAT_WORKSTATION_0, *LPSTAT_WORKSTATION_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmstats.h
api_name:
-	STAT_WORKSTATION_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _STAT_WORKSTATION_0 structure


## -description


Contains statistical information about the specified workstation.


## -struct-fields




### -field stw0_start

 


### -field stw0_numNCB_r

 


### -field stw0_numNCB_s

 


### -field stw0_numNCB_a

 


### -field stw0_fiNCB_r

 


### -field stw0_fiNCB_s

 


### -field stw0_fiNCB_a

 


### -field stw0_fcNCB_r

 


### -field stw0_fcNCB_s

 


### -field stw0_fcNCB_a

 


### -field stw0_sesstart

 


### -field stw0_sessfailcon

 


### -field stw0_sessbroke

 


### -field stw0_uses

 


### -field stw0_usefail

 


### -field stw0_autorec

 


### -field stw0_bytessent_r_lo

 


### -field stw0_bytessent_r_hi

 


### -field stw0_bytesrcvd_r_lo

 


### -field stw0_bytesrcvd_r_hi

 


### -field stw0_bytessent_s_lo

 


### -field stw0_bytessent_s_hi

 


### -field stw0_bytesrcvd_s_lo

 


### -field stw0_bytesrcvd_s_hi

 


### -field stw0_bytessent_a_lo

 


### -field stw0_bytessent_a_hi

 


### -field stw0_bytesrcvd_a_lo

 


### -field stw0_bytesrcvd_a_hi

 


### -field stw0_reqbufneed

 


### -field stw0_bigbufneed

 




#### - BytesReceived

Specifies the total number of bytes received by the workstation.


#### - BytesTransmitted

Specifies the total number of bytes transmitted by the workstation.


#### - CacheReadBytesRequested

Specifies the total number of bytes that have been read by cache I/O requests.


#### - CacheWriteBytesRequested

Specifies the total number of bytes that have been written by cache I/O requests.


#### - CoreConnects

Specifies the total number of connections to servers supporting the PCNET dialect that have succeeded.


#### - CurrentCommands

Specifies the number of current requests that have not been completed.


#### - FailedCompletionOperations

Specifies the total number of network operations that failed to complete.


#### - FailedSessions

Specifies the number of times the workstation attempted to create a session but failed.


#### - FailedUseCount

Specifies the total number of failed network connections for the workstation.


#### - HungSessions

Specifies the total number of sessions that have expired on the workstation.


#### - InitiallyFailedOperations

Specifies the total number of network operations that failed to begin.


#### - Lanman20Connects

Specifies the total number of connections to servers supporting the LanManager 2.0 dialect that have succeeded.


#### - Lanman21Connects

Specifies the total number of connections to servers supporting the LanManager 2.1 dialect that have succeeded.


#### - LanmanNtConnects

Specifies the total number of connections to servers supporting the NTLM dialect that have succeeded.


#### - LargeReadSmbs

Specifies the total number of read requests the workstation has sent to servers that are greater than twice the size of the server's negotiated buffer size.


#### - LargeWriteSmbs

Specifies the total number of write requests the workstation has sent to servers that are greater than twice the size of the server's negotiated buffer size.


#### - NetworkErrors

Specifies the total number of network errors received by the workstation.


#### - NetworkReadBytesRequested

Specifies the total amount of bytes that have been read by disk I/O requests.


#### - NetworkWriteBytesRequested

Specifies the total number of bytes that have been written by disk I/O requests.


#### - NonPagingReadBytesRequested

Specifies the total number of bytes that have been read by non-paging I/O requests.


#### - NonPagingWriteBytesRequested

Specifies the total number of bytes that have been written by non-paging I/O requests.


#### - PagingReadBytesRequested

Specifies the total number of bytes that have been read by paging I/O requests.


#### - PagingWriteBytesRequested

Specifies the total number of bytes that have been written by paging I/O requests.


#### - RandomReadOperations

Specifies the total number of random access reads initiated by the workstation.


#### - RandomWriteOperations

Specifies the total number of random access writes initiated by the workstation.


#### - RawReadsDenied

Specifies the total number of raw read requests made by the workstation that have been denied.


#### - RawWritesDenied

Specifies the total number of raw write requests made by the workstation that have been denied.


#### - ReadOperations

Specifies the total number of read operations initiated by the workstation.


#### - ReadSmbs

Specifies the total number of read requests the workstation has sent to servers.


#### - Reconnects

Specifies the total number of connections that have failed.


#### - ServerDisconnects

Specifies the number of times the workstation was disconnected by a network server.


#### - Sessions

Specifies the total number of workstation sessions that were established.


#### - SmallReadSmbs

Specifies the total number of read requests the workstation has sent to servers that are less than 1/4 of the size of the server's negotiated buffer size.


#### - SmallWriteSmbs

Specifies the total number of write requests the workstation has sent to servers that are less than 1/4 of the size of the server's negotiated buffer size.


#### - SmbsReceived

Specifies the total number of server message blocks (SMBs) received by the workstation.


#### - SmbsTransmitted

Specifies the total number of SMBs transmitted by the workstation.


#### - StatisticsStartTime

Specifies the time statistics collection started. This member also indicates when statistics for the workstations were last cleared. The value is stored as the number of seconds elapsed since 00:00:00, January 1, 1970.


#### - UseCount

Specifies the total number of network connections established by the workstation.


#### - WriteOperations

Specifies the total number of write operations initiated by the workstation.


#### - WriteSmbs

Specifies the total number of write requests the workstation has sent to servers.


## -see-also




<a href="https://msdn.microsoft.com/d0e51d8a-2f54-42ca-9759-0da82c1f0f55">NetStatisticsGet</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/4e0217bf-7550-40a2-b47c-8e898a586005">Statistics Functions</a>
 

 

