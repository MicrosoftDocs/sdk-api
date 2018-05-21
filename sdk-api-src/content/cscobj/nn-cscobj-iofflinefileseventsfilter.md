---
UID: NN:cscobj.IOfflineFilesEventsFilter
title: IOfflineFilesEventsFilter
author: windows-driver-content
description: Provides a mechanism for recipients of published events to restrict the number of event instances they receive.
old-location: of\iofflinefileseventsfilter.htm
old-project: OfflineFiles
ms.assetid: 8c2c793e-c91c-4ca7-a03c-e349de00de6c
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: IOfflineFilesEventsFilter, IOfflineFilesEventsFilter interface [Offline Files], IOfflineFilesEventsFilter interface [Offline Files],described, cscobj/IOfflineFilesEventsFilter, of.iofflinefileseventsfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IOfflineFilesEventsFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEventsFilter interface


## -description


Provides a mechanism for recipients of published events to restrict the number of event instances they receive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEventsFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesEventsFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesEventsFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40e388b2-b051-4b0a-b96e-7a73b521758e">GetExcludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should not be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb10da3-7566-43f7-8349-f94e59e12907">GetIncludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/4ab65756-5985-4240-805d-2221db3d1459">OFFLINEFILES_EVENTS</a> enumeration values describing which events should be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b9d8339-3daa-4f0c-8a52-59e06b663163">GetPathFilter</a>
</td>
<td align="left" width="63%">
Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

