---
UID: NN:cscobj.IOfflineFilesEventsFilter
title: IOfflineFilesEventsFilter
author: windows-sdk-content
description: Provides a mechanism for recipients of published events to restrict the number of event instances they receive.
old-location: of\iofflinefileseventsfilter.htm
tech.root: OfflineFiles
ms.assetid: 8c2c793e-c91c-4ca7-a03c-e349de00de6c
ms.author: windowssdkdev
ms.date: 09/26/2018
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
 - IOfflineFilesEventsFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEventsFilter interface


## -description


Provides a mechanism for recipients of published events to restrict the number of event instances they receive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEventsFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesEventsFilter</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530533(v=VS.85).aspx">GetExcludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/en-us/library/Bb530645(v=VS.85).aspx">OFFLINEFILES_EVENTS</a> enumeration values describing which events should not be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530535(v=VS.85).aspx">GetIncludedEvents</a>
</td>
<td align="left" width="63%">
Retrieves an array of <a href="https://msdn.microsoft.com/en-us/library/Bb530645(v=VS.85).aspx">OFFLINEFILES_EVENTS</a> enumeration values describing which events should be received by the event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530536(v=VS.85).aspx">GetPathFilter</a>
</td>
<td align="left" width="63%">
Retrieves a UNC path string and a scope indicator describing which path-based events should be delivered to this event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

