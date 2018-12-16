---
UID: NN:qmgr.IEnumBackgroundCopyGroups
title: IEnumBackgroundCopyGroups
author: windows-sdk-content
description: Use the IEnumBackgroundCopyGroups interface to enumerate the list of groups in the download queue. To get an IEnumBackgroundCopyGroups interface pointer, call the IBackgroundCopyQMgr::EnumGroups method.
old-location: bits\ienumbackgroundcopygroups.htm
tech.root: bits
ms.assetid: 64a05103-9749-41fd-9987-8bb17b9284f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumBackgroundCopyGroups, IEnumBackgroundCopyGroups interface [BITS], IEnumBackgroundCopyGroups interface [BITS],described, bits.ienumbackgroundcopygroups, qmgr/IEnumBackgroundCopyGroups
ms.topic: interface
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyGroups
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBackgroundCopyGroups interface


## -description


<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>IEnumBackgroundCopyGroups</b> interface to enumerate the list of groups in the download queue. To get an <b>IEnumBackgroundCopyGroups</b> interface pointer, call the <a href="https://msdn.microsoft.com/27cf17e3-b35a-4453-ae0a-8b080fd120dc">IBackgroundCopyQMgr::EnumGroups</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBackgroundCopyGroups</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumBackgroundCopyGroups</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBackgroundCopyGroups</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2743edd-9fc5-451b-b1ff-17f4591923ba">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70bbc495-f133-4703-a51a-1a1a180720f4">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc21f663-e8f8-4348-920c-bffad46d0aa0">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16bcfd69-9fb2-4214-8a7d-4188c6516ebb">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27e907d0-1b2a-44d2-b401-0b28d5a8b340">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

