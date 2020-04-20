---
UID: NN:winsync.ISyncFilterInfo2
title: ISyncFilterInfo2 (winsync.h)
description: Represents additional information about a filter that can be used to control which changes are included in an ISyncChangeBatch object.helpviewer_keywords: ["ISyncFilterInfo2","ISyncFilterInfo2 interface [Windows Sync]","ISyncFilterInfo2 interface [Windows Sync]","described","winsync.isyncfilterinfo2","winsync/ISyncFilterInfo2"]
old-location: winsync\isyncfilterinfo2.htm
tech.root: winsync
ms.assetid: b1ffc6a7-ca82-4ce6-b7ac-c4c39c59891d
ms.date: 12/05/2018
ms.keywords: ISyncFilterInfo2, ISyncFilterInfo2 interface [Windows Sync], ISyncFilterInfo2 interface [Windows Sync],described, winsync.isyncfilterinfo2, winsync/ISyncFilterInfo2
f1_keywords:
- winsync/ISyncFilterInfo2
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
- ISyncFilterInfo2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncFilterInfo2 interface


## -description


Represents additional information about a filter that can be used to control which changes are included in an <b>ISyncChangeBatch</b> object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFilterInfo2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo</a>. <b>ISyncFilterInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFilterInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncfilterinfo2-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags that specify additional information about the filter information object.


</td>
</tr>
</table> 


## -remarks



<b>ISyncFilterInfo2</b> can obtained by calling <b>QueryInterface</b> on an <b>ISyncFilterInfo</b> object or an object derived from <b>ISyncFilterInfo</b>, such as an <b>IChangeUnitListFilterInfo</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

