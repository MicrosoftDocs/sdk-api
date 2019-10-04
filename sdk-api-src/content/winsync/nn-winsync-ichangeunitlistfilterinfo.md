---
UID: NN:winsync.IChangeUnitListFilterInfo
title: IChangeUnitListFilterInfo (winsync.h)
author: windows-sdk-content
description: Represents a filter that can be used to control which change units are included for items in an ISyncChangeBatch object.
old-location: winsync\ichangeunitlistfilterinfo.htm
tech.root: winsync
ms.assetid: fd379fc6-22e5-4165-b4e6-480bc65cccb3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IChangeUnitListFilterInfo, IChangeUnitListFilterInfo interface [Windows Sync], IChangeUnitListFilterInfo interface [Windows Sync],described, winsync.ichangeunitlistfilterinfo, winsync/IChangeUnitListFilterInfo
ms.topic: interface
f1_keywords: 
 - "winsync/IChangeUnitListFilterInfo"
dev_langs:
 - c++
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
 - IChangeUnitListFilterInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IChangeUnitListFilterInfo interface


## -description


Represents a filter that can be used to control which change units are included for items in an <b>ISyncChangeBatch</b> object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChangeUnitListFilterInfo</b> interface inherits from <b>ISyncFilterInfo</b>. <b>IChangeUnitListFilterInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChangeUnitListFilterInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitlistfilterinfo-getchangeunitid">GetChangeUnitId</a>
</td>
<td align="left" width="63%">
Gets the change unit ID that is stored at the specified index in the array of change unit IDs that define the filter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitlistfilterinfo-getchangeunitidcount">GetChangeUnitIdCount</a>
</td>
<td align="left" width="63%">
Gets the number of change unit IDs that define the filter. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitlistfilterinfo-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a new instance of the <b>IChangeUnitListFilterInfo</b> class that contains the specified array of change unit IDs.


</td>
</tr>
</table> 


## -remarks



If a provider filters the contents of a change batch that it creates, it must create a filtered <b>ISyncChangeBatch</b> object instead of a standard change batch object. The filtered change batch object contains an <b>IChangeUnitListFilterInfo</b> object that describes how the contents of the change batch were filtered.




## -see-also




<b>ISyncFilterInfo</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

