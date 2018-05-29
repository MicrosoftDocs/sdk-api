---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0004
title: "__MIDL___MIDL_itf_pla_0001_0043_0004"
author: windows-sdk-content
description: Defines the running status of the data collector set.
old-location: pla\datacollectorsetstatus.htm
old-project: PLA
ms.assetid: 7cccb588-c530-46dc-99e8-84e763cb0a8b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DataCollectorSetStatus, DataCollectorSetStatus enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0004, base.datacollectorsetstatus, pla.datacollectorsetstatus, pla/DataCollectorSetStatus, pla/plaCompiling, pla/plaPending, pla/plaRunning, pla/plaStopped, pla/plaUndefined, plaCompiling, plaPending, plaRunning, plaStopped, plaUndefined
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DataCollectorSetStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pla.h
api_name:
-	DataCollectorSetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_pla_0001_0043_0004 enumeration


## -description


Defines the running status of the data collector set.


## -enum-fields




### -field plaStopped

The data collector set is not running.


### -field plaRunning

The data collector set is running.


### -field plaCompiling

The data collector set is performing data management. A running data collector set will transition from <b>plaRunning</b> to <b>plaCompiling</b> if the data manager is enabled.


### -field plaPending

The data collector has been set to run, but the service has not started it yet.  Only computers that run operating systems prior to Windows Vista report this status.


### -field plaUndefined

Cannot determine the status but no error has occurred. Typically, this status is set for autologgers.


## -see-also




<a href="https://msdn.microsoft.com/d957d34d-5455-486a-bd54-28afd7e6f979">IDataCollectorSet::Status</a>
 

 

