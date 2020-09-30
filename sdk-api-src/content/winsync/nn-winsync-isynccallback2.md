---
UID: NN:winsync.ISyncCallback2
title: ISyncCallback2 (winsync.h)
description: Represents additional application callbacks that are used to notify the application of synchronization events.
helpviewer_keywords: ["ISyncCallback2","ISyncCallback2 interface [Windows Sync]","ISyncCallback2 interface [Windows Sync]","described","winsync.isynccallback2","winsync/ISyncCallback2"]
old-location: winsync\isynccallback2.htm
tech.root: winsync
ms.assetid: d2d690ba-8da2-4d53-a42c-14e4f010bc2d
ms.date: 12/05/2018
ms.keywords: ISyncCallback2, ISyncCallback2 interface [Windows Sync], ISyncCallback2 interface [Windows Sync],described, winsync.isynccallback2, winsync/ISyncCallback2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncCallback2
 - winsync/ISyncCallback2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncCallback2
---

# ISyncCallback2 interface


## -description

Represents additional application callbacks that are used to notify the application of synchronization events.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncCallback2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback</a>. <b>ISyncCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback2-onchangeapplied">OnChangeApplied</a>
</td>
<td align="left" width="63%">
Occurs after a change is successfully applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback2-onchangefailed">OnChangeFailed</a>
</td>
<td align="left" width="63%">
Occurs after a change fails to apply.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/winsync/ne-winsync-conflict_resolution_policy">CONFLICT_RESOLUTION_POLICY Enumeration</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>