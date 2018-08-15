---
UID: NE:resapi.LOG_LEVEL
title: LOG_LEVEL
author: windows-sdk-content
description: Represents the severity of the log event passed to the LogEvent callback function.
old-location: mscs\log_level.htm
old-project: mscs
ms.assetid: 976251d5-6619-47f7-9b6e-2031768100b0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLOG_LEVEL, LOG_ERROR, LOG_INFORMATION, LOG_LEVEL, LOG_LEVEL enumeration [Failover Cluster], LOG_SEVERE, LOG_WARNING, PLOG_LEVEL, PLOG_LEVEL enumeration pointer [Failover Cluster], mscs.log_level, resapi/LOG_ERROR, resapi/LOG_INFORMATION, resapi/LOG_LEVEL, resapi/LOG_SEVERE, resapi/LOG_WARNING, resapi/PLOG_LEVEL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: resapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: LOG_LEVEL, *PLOG_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - LOG_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# LOG_LEVEL enumeration


## -description


Represents the severity of the log event passed to the 
    <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> callback function.


## -enum-fields




### -field LOG_INFORMATION

The event is informational.


### -field LOG_WARNING

The event is reporting a failure that might have happened, but it is uncertain whether a failure really did 
      occur.


### -field LOG_ERROR

The event affects a single component, but other components are not affected and the integrity of the rest 
      of the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> is not compromised.


### -field LOG_SEVERE

The event is reporting a severe failure that affects multiple components, or the integrity of the entire 
      system is compromised or believed to be compromised.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a>
 

 

