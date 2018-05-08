---
UID: NN:cscobj.IOfflineFilesEvents2
title: IOfflineFilesEvents2
author: windows-driver-content
description: Used to report additional events associated with Offline Files.
old-location: of\iofflinefilesevents2.htm
old-project: OfflineFiles
ms.assetid: 746f7220-8c87-4218-bd97-ec9b862e549c
ms.author: windowsdriverdev
ms.date: 2/15/2018
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
-	IOfflineFilesEvents2
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesEvents2 interface


## -description


 Used to report additional events associated with Offline Files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesEvents2</b> interface inherits from <a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>. <b>IOfflineFilesEvents2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/84b71228-904a-4042-8d13-422ae77f7ba5">BackgroundSyncBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service is beginning to perform a background synchronization pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41a2152-8100-47a7-a994-a0fe9fae4dc4">BackgroundSyncEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service completed a background synchronization pass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be1c5e7f-d3fe-4cf7-99ef-6c055b07aba6">CacheEvictBegin</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08af0c55-17cc-4d7f-b4a3-c21a8ae91b74">CacheEvictEnd</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b0d112d-17be-481a-8793-2b57506ec7b2">ItemReconnectBegin</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service is beginning to attempt to reconnect all offline scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/929d6556-69cb-4863-a665-236603fcd88b">ItemReconnectEnd</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service has completed its attempt to reconnect all offline scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1009c67a-09f4-40ea-8aa9-fb42f1ab54ff">PolicyChangeDetected</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service detected a change in one or more of its setting values that are controlled by Group Policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c947d9e5-2712-4dbd-8806-79a8bf0f4cc9">PreferenceChangeDetected</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service detected a change in one or more of its setting values that are not controlled by Group Policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af59c8ac-ecd4-48e7-9ebb-8802e7d6ffef">SettingsChangesApplied</a>
</td>
<td align="left" width="63%">
Reports that the Offline Files service has applied the changes that were detected in Group Policy or preference values.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c0bd0033-e5e1-4d21-8d98-eb937acdd6cf">IOfflineFilesEvents</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

