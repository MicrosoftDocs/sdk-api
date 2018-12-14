---
UID: NS:wtsdefs._WTS_PROTOCOL_STATUS
title: WTS_PROTOCOL_STATUS
author: windows-sdk-content
description: Contains information about the status of the protocol.
old-location: termserv\wts_protocol_status.htm
tech.root: TermServ
ms.assetid: 20e66033-fc79-49c9-af0e-abaf6e4ba501
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWTS_PROTOCOL_STATUS, PWRDS_PROTOCOL_STATUS, PWRDS_PROTOCOL_STATUS structure pointer [Remote Desktop Services], PWTS_PROTOCOL_STATUS, PWTS_PROTOCOL_STATUS structure pointer [Remote Desktop Services], WRDS_PROTOCOL_STATUS, WRDS_PROTOCOL_STATUS structure [Remote Desktop Services], WTS_PROTOCOL_STATUS, WTS_PROTOCOL_STATUS structure [Remote Desktop Services], termserv.wts_protocol_status, wtsdefs/PWRDS_PROTOCOL_STATUS, wtsdefs/PWTS_PROTOCOL_STATUS, wtsdefs/WRDS_PROTOCOL_STATUS, wtsdefs/WTS_PROTOCOL_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsdefs.h
api_name:
 - WTS_PROTOCOL_STATUS
product: Windows
targetos: Windows
req.typenames: WTS_PROTOCOL_STATUS, *PWTS_PROTOCOL_STATUS
req.redist: 
---

# WTS_PROTOCOL_STATUS structure


## -description


Contains information about the status of the protocol.


## -struct-fields




### -field Output

A <a href="https://msdn.microsoft.com/118c5e12-5436-4c0a-a31d-a60c5123e384">WTS_PROTOCOL_COUNTERS</a> structure that contains the output protocol counters.


### -field Input

A <a href="https://msdn.microsoft.com/118c5e12-5436-4c0a-a31d-a60c5123e384">WTS_PROTOCOL_COUNTERS</a> structure that contains the input protocol counters.


### -field Cache

A <a href="https://msdn.microsoft.com/3c29596f-77c6-415b-bf97-529f70b9d9fe">WTS_CACHE_STATS</a> structure that contains protocol cache statistics.


### -field AsyncSignal

An integer that identifies an asynchronous signal for asynchronous protocols.


### -field AsyncSignalMask

An asynchronous signal mask.


### -field Counters

An array of up to 100 counters.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/d224877a-649a-4ac2-a5e7-831592e6a0d9">GetProtocolStatus</a> method.



