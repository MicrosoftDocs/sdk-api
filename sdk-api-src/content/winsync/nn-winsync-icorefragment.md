---
UID: NN:winsync.ICoreFragment
title: ICoreFragment
author: windows-driver-content
description: Represents knowledge of all items in the scope for a specific set of change units.
old-location: winsync\icorefragment.htm
old-project: winsync
ms.assetid: 3e232531-ad44-4ad1-b186-46edbc07291b
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ICoreFragment, ICoreFragment interface [Windows Sync], ICoreFragment interface [Windows Sync],described, winsync.icorefragment, winsync/ICoreFragment
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ICoreFragment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ICoreFragment interface


## -description


Represents knowledge of all items in the scope for a specific set of change units.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreFragment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICoreFragment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICoreFragment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f1aff6d-4fdf-48e1-9c7b-c003ec27f354">GetColumnCount</a>
</td>
<td align="left" width="63%">
Gets the number of columns that are contained in this knowledge fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eb33224-f017-4f3b-bbf9-14d388d0868f">GetRangeCount</a>
</td>
<td align="left" width="63%">
Gets the number of ranges that are contained in this knowledge fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d50527cb-00ba-4e7b-9fb3-267eaa6cd6e6">NextColumn</a>
</td>
<td align="left" width="63%">
Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25cfd4f5-2ff1-47eb-8cc0-17e17efa4ec2">NextRange</a>
</td>
<td align="left" width="63%">
Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets both the column and range enumerators to the beginning of their respective sets.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects, each of which contains knowledge that applies to a specific set of change units. Typically, one of the <b>ICoreFragment</b> objects contains no change unit IDs. The knowledge that is contained in the <b>ICoreFragment</b> object that contains no change unit IDs applies to all change unit IDs that are not otherwise contained in another <b>ICoreFragment</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

