---
UID: NF:cscobj.IOfflineFilesEvents.DataLost
title: IOfflineFilesEvents::DataLost
author: windows-sdk-content
description: Reports that one or more events destined for this event sink have been lost and will not be delivered.
old-location: of\iofflinefilesevents_datalost.htm
old-project: OfflineFiles
ms.assetid: da0414dd-2acb-48d9-ac84-66bb1f7ccbef
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DataLost, DataLost method [Offline Files], DataLost method [Offline Files],IOfflineFilesEvents interface, IOfflineFilesEvents interface [Offline Files],DataLost method, IOfflineFilesEvents.DataLost, IOfflineFilesEvents::DataLost, cscobj/IOfflineFilesEvents::DataLost, of.iofflinefilesevents_datalost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesEvents.DataLost
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::DataLost


## -description



    Reports that one or more events destined for this event sink have been lost and will not be delivered. The receipt of this event indicates that the service is attempting to deliver events to this event sink faster than the sink is consuming them.


## -parameters






## -returns



The return value is ignored.




## -remarks



This event cannot be filtered out by using the <a href="https://msdn.microsoft.com/8c2c793e-c91c-4ca7-a03c-e349de00de6c">IOfflineFilesEventsFilter</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

