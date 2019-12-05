---
UID: NN:winsync.ISyncChangeBatchBase2
title: ISyncChangeBatchBase2 (winsync.h)
description: Represents additional capabilities of an ISyncChangeBatchBase object.
old-location: winsync\isyncchangebatchbase2.htm
tech.root: winsync
ms.assetid: 45f10ed0-b3ce-41f5-b2d9-9166bff2abec
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase2, ISyncChangeBatchBase2 interface [Windows Sync], ISyncChangeBatchBase2 interface [Windows Sync],described, winsync.isyncchangebatchbase2, winsync/ISyncChangeBatchBase2
ms.topic: interface
f1_keywords:
- winsync/ISyncChangeBatchBase2
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
- ISyncChangeBatchBase2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchBase2 interface


## -description


Represents additional capabilities of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchBase2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a>. <b>ISyncChangeBatchBase2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchBase2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchbase2-serializewithoptions">SerializeWithOptions</a>
</td>
<td align="left" width="63%">
Serializes the change batch object data to a byte array based on the specified version and serialization options.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchBase2</b> object can be obtained by passing <b>IID_ISyncChangeBatchBase2</b> to the <b>QueryInterface</b> method of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a> object.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchanges">IEnumSyncChanges Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://docs.microsoft.com/windows/win32/api/winsync/ne-winsync-sync_serialization_version">SyncSerializationVersion Enumeration</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

