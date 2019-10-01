---
UID: NN:winsync.ICoreFragment
title: ICoreFragment (winsync.h)
author: windows-sdk-content
description: Represents knowledge of all items in the scope for a specific set of change units.
old-location: winsync\icorefragment.htm
tech.root: winsync
ms.assetid: 3e232531-ad44-4ad1-b186-46edbc07291b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICoreFragment, ICoreFragment interface [Windows Sync], ICoreFragment interface [Windows Sync],described, winsync.icorefragment, winsync/ICoreFragment
ms.topic: interface
f1_keywords: 
 - "winsync/ICoreFragment"
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
 - ICoreFragment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICoreFragment interface


## -description


Represents knowledge of all items in the scope for a specific set of change units.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreFragment</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICoreFragment</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-icorefragment-getcolumncount">GetColumnCount</a>
</td>
<td align="left" width="63%">
Gets the number of columns that are contained in this knowledge fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-icorefragment-getrangecount">GetRangeCount</a>
</td>
<td align="left" width="63%">
Gets the number of ranges that are contained in this knowledge fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-icorefragment-nextcolumn">NextColumn</a>
</td>
<td align="left" width="63%">
Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-icorefragment-nextrange">NextRange</a>
</td>
<td align="left" width="63%">
Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-icorefragment-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets both the column and range enumerators to the beginning of their respective sets.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects, each of which contains knowledge that applies to a specific set of change units. Typically, one of the <b>ICoreFragment</b> objects contains no change unit IDs. The knowledge that is contained in the <b>ICoreFragment</b> object that contains no change unit IDs applies to all change unit IDs that are not otherwise contained in another <b>ICoreFragment</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

