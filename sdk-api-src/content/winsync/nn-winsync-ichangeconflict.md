---
UID: NN:winsync.IChangeConflict
title: IChangeConflict
author: windows-sdk-content
description: Represents a conflict between two items.
old-location: winsync\ichangeconflict.htm
old-project: winsync
ms.assetid: b0089d3d-a1e6-4662-9e79-4c0b22c08d7f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IChangeConflict, IChangeConflict interface [Windows Sync], IChangeConflict interface [Windows Sync],described, winsync.ichangeconflict, winsync/IChangeConflict
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeConflict
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeConflict interface


## -description


Represents a conflict between two items.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChangeConflict</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IChangeConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChangeConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4624f92a-8455-4490-a256-9cf849626844">GetDestinationProviderConflictingChange</a>
</td>
<td align="left" width="63%">
Gets the change metadata from the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a63d554-56e0-4c39-94ea-613fecc97331">GetDestinationProviderConflictingData</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to retrieve item data for the change item from the destination replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b89124fe-200e-4061-974e-2d686de7a932">GetResolveActionForChange</a>
</td>
<td align="left" width="63%">
Gets the conflict resolution action for the conflict.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/206ee654-e8a6-4b71-b933-3380dc4ed0ad">GetResolveActionForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the conflict resolution action for the conflicting change unit change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a77983ec-77fd-4e24-a978-df37a85b0ede">GetSourceProviderConflictingChange</a>
</td>
<td align="left" width="63%">
Gets the change metadata from the source provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4227b559-59e9-4b87-beb0-2d47f3d81414">GetSourceProviderConflictingData</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to retrieve item data for the change item from the source replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1a26c85-a00d-408e-96ea-5849c6bb99ff">SetResolveActionForChange</a>
</td>
<td align="left" width="63%">
Sets a conflict resolution action for the conflict.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8594a888-21a1-4cfb-964c-9c670e3a7438">SetResolveActionForChangeUnit</a>
</td>
<td align="left" width="63%">
Sets a conflict resolution action for the conflicting change unit change.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

