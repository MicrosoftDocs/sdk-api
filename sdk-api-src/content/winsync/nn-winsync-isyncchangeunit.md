---
UID: NN:winsync.ISyncChangeUnit
title: ISyncChangeUnit
author: windows-sdk-content
description: Represents a change to a change unit that is contained in an item.
old-location: winsync\isyncchangeunit.htm
old-project: winsync
ms.assetid: 6c889a78-1a50-47b5-8e49-4aba741c0be0
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeUnit, ISyncChangeUnit interface [Windows Sync], ISyncChangeUnit interface [Windows Sync],described, winsync.isyncchangeunit, winsync/ISyncChangeUnit
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeUnit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeUnit interface


## -description


Represents a change to a change unit that is contained in an item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeUnit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncChangeUnit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeUnit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/956f2d51-3b14-4bbd-8a29-6d63aa3c344f">GetChangeUnitId</a>
</td>
<td align="left" width="63%">
Gets the change unit ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b40ec132-0459-4ddf-9156-bce2a1dfbc4d">GetChangeUnitVersion</a>
</td>
<td align="left" width="63%">
Gets the version for the change unit change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d28b4eb0-ddd2-4abf-9183-4d39b728923b">GetItemChange</a>
</td>
<td align="left" width="63%">
Gets the item change that contains this change unit change.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

