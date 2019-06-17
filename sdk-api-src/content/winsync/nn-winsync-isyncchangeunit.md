---
UID: NN:winsync.ISyncChangeUnit
title: ISyncChangeUnit (winsync.h)
author: windows-sdk-content
description: Represents a change to a change unit that is contained in an item.
old-location: winsync\isyncchangeunit.htm
tech.root: winsync
ms.assetid: 6c889a78-1a50-47b5-8e49-4aba741c0be0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeUnit, ISyncChangeUnit interface [Windows Sync], ISyncChangeUnit interface [Windows Sync],described, winsync.isyncchangeunit, winsync/ISyncChangeUnit
ms.topic: interface
f1_keywords: ["winsync/ISyncChangeUnit"]
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
 - ISyncChangeUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeUnit interface


## -description


Represents a change to a change unit that is contained in an item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeUnit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeUnit</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangeunit-getchangeunitid">GetChangeUnitId</a>
</td>
<td align="left" width="63%">
Gets the change unit ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangeunit-getchangeunitversion">GetChangeUnitVersion</a>
</td>
<td align="left" width="63%">
Gets the version for the change unit change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangeunit-getitemchange">GetItemChange</a>
</td>
<td align="left" width="63%">
Gets the item change that contains this change unit change.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

