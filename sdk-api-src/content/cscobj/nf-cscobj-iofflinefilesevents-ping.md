---
UID: NF:cscobj.IOfflineFilesEvents.Ping
title: IOfflineFilesEvents::Ping
author: windows-sdk-content
description: This event is delivered to all registered event subscribers on a periodic basis.
old-location: of\iofflinefilesevents_ping.htm
tech.root: OfflineFiles
ms.assetid: edde2f37-f082-4382-8908-181bc42d30ef
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],Ping method, IOfflineFilesEvents.Ping, IOfflineFilesEvents::Ping, Ping, Ping method [Offline Files], Ping method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::Ping, of.iofflinefilesevents_ping
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
 - IOfflineFilesEvents.Ping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents::Ping


## -description


This event is delivered to all registered event subscribers on a periodic basis.


## -parameters






## -returns



The return value is ignored.




## -remarks



If a recipient does not respond, a COM error is received by the Offline Files service, and the subscriber's connection is deleted.  This is how the Offline Files service detects event subscriber processes that have terminated before calling <a href="https://msdn.microsoft.com/en-us/library/ms686608(v=VS.85).aspx">IConnectionPoint::Unadvise</a>.

This event cannot be filtered out by using the <a href="https://msdn.microsoft.com/en-us/library/Bb530532(v=VS.85).aspx">IOfflineFilesEventsFilter</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>
 

 

