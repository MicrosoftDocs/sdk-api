---
UID: NF:cscobj.IOfflineFilesEvents.DataLost
title: IOfflineFilesEvents::DataLost
author: windows-sdk-content
description: Reports that one or more events destined for this event sink have been lost and will not be delivered.
old-location: of\iofflinefilesevents_datalost.htm
tech.root: offlinefiles
ms.assetid: da0414dd-2acb-48d9-ac84-66bb1f7ccbef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DataLost, DataLost method [Offline Files], DataLost method [Offline Files],IOfflineFilesEvents interface, IOfflineFilesEvents interface [Offline Files],DataLost method, IOfflineFilesEvents.DataLost, IOfflineFilesEvents::DataLost, cscobj/IOfflineFilesEvents::DataLost, of.iofflinefilesevents_datalost
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::DataLost


## -description


Reports that one or more events destined for this event sink have been lost and will not be delivered. The receipt of this event indicates that the service is attempting to deliver events to this event sink faster than the sink is consuming them.


## -parameters






## -returns



The return value is ignored.




## -remarks



This event cannot be filtered out by using the <a href="https://msdn.microsoft.com/en-us/library/Bb530532(v=VS.85).aspx">IOfflineFilesEventsFilter</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

