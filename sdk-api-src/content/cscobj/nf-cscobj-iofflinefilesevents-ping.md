---
UID: NF:cscobj.IOfflineFilesEvents.Ping
title: IOfflineFilesEvents::Ping
author: windows-sdk-content
description: This event is delivered to all registered event subscribers on a periodic basis.
old-location: of\iofflinefilesevents_ping.htm
old-project: OfflineFiles
ms.assetid: edde2f37-f082-4382-8908-181bc42d30ef
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],Ping method, IOfflineFilesEvents.Ping, IOfflineFilesEvents::Ping, Ping, Ping method [Offline Files], Ping method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::Ping, of.iofflinefilesevents_ping
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesEvents.Ping
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents::Ping


## -description



    This event is delivered to all registered event subscribers on a periodic basis.
   


## -parameters






## -returns



The return value is ignored.




## -remarks



If a recipient does not respond, a COM error is received by the Offline Files service, and the subscriber's connection is deleted.  This is how the Offline Files service detects event subscriber processes that have terminated before calling <a href="_com_iconnectionpoint_unadvise">IConnectionPoint::Unadvise</a>.

This event cannot be filtered out by using the <a href="https://msdn.microsoft.com/8c2c793e-c91c-4ca7-a03c-e349de00de6c">IOfflineFilesEventsFilter</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>
 

 

