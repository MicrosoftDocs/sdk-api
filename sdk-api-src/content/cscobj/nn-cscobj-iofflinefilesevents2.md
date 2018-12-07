---
UID: NN:cscobj.IOfflineFilesEvents2
title: IOfflineFilesEvents2
author: windows-sdk-content
description: Used to report additional events associated with Offline Files.
old-location: of\iofflinefilesevents2.htm
tech.root: offlinefiles
ms.assetid: 746f7220-8c87-4218-bd97-ec9b862e549c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesEvents2, IOfflineFilesEvents2 interface [Offline Files], IOfflineFilesEvents2 interface [Offline Files],described, cscobj/IOfflineFilesEvents2, of.iofflinefilesevents2
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
 - IOfflineFilesEvents2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesEvents2 interface


## -description


 Used to report additional events associated with Offline Files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>. <b>IOfflineFilesEvents2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesEvents2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530522(v=VS.85).aspx">BackgroundSyncBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service is beginning to perform a background synchronization pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530524(v=VS.85).aspx">BackgroundSyncEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service completed a background synchronization pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530525(v=VS.85).aspx">CacheEvictBegin</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530526(v=VS.85).aspx">CacheEvictEnd</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530527(v=VS.85).aspx">ItemReconnectBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service is beginning to attempt to reconnect all offline scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530528(v=VS.85).aspx">ItemReconnectEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service has completed its attempt to reconnect all offline scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530529(v=VS.85).aspx">PolicyChangeDetected</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service detected a change in one or more of its setting values that are controlled by Group Policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530530(v=VS.85).aspx">PreferenceChangeDetected</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service detected a change in one or more of its setting values that are not controlled by Group Policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530531(v=VS.85).aspx">SettingsChangesApplied</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service has applied the changes that were detected in Group Policy or preference values.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530520(v=VS.85).aspx">IOfflineFilesEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

