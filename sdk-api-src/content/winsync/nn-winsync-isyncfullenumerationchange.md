---
UID: NN:winsync.ISyncFullEnumerationChange
title: ISyncFullEnumerationChange
author: windows-sdk-content
description: Represents additional information about an ISyncChange object during recovery synchronization.
old-location: winsync\isyncfullenumerationchange.htm
tech.root: winsync
ms.assetid: 1e666737-c5dc-4394-9f41-6e77832dd9f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncFullEnumerationChange, ISyncFullEnumerationChange interface [Windows Sync], ISyncFullEnumerationChange interface [Windows Sync],described, winsync.isyncfullenumerationchange, winsync/ISyncFullEnumerationChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncFullEnumerationChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncFullEnumerationChange interface


## -description


Represents additional information about an <b>ISyncChange</b> object during recovery synchronization.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFullEnumerationChange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncFullEnumerationChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFullEnumerationChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/958bca82-67a7-401f-a9d3-a17f60496cba">GetLearnedForgottenKnowledge</a>
</td>
<td align="left" width="63%">
Gets the forgotten knowledge that the destination replica learns when the destination provider applies this change during recovery synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6d536ad-557a-489d-a3e3-a4ffd69be096">GetLearnedKnowledgeAfterRecoveryComplete</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica will learn after it applies this change during recovery synchronization.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>ISyncFullEnumerationChange</b> object, pass <b>IID_ISyncFullEnumerationChange</b> to the <b>QueryInterface</b> method of an <a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange</a> object during recovery synchronization.




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

