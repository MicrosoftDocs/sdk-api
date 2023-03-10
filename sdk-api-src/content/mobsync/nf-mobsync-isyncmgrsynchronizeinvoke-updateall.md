---
UID: NF:mobsync.ISyncMgrSynchronizeInvoke.UpdateAll
title: ISyncMgrSynchronizeInvoke::UpdateAll (mobsync.h)
description: Programmatically starts an update for all items.
helpviewer_keywords: ["ISyncMgrSynchronizeInvoke interface [Windows Shell]","UpdateAll method","ISyncMgrSynchronizeInvoke.UpdateAll","ISyncMgrSynchronizeInvoke::UpdateAll","UpdateAll","UpdateAll method [Windows Shell]","UpdateAll method [Windows Shell]","ISyncMgrSynchronizeInvoke interface","mobsync/ISyncMgrSynchronizeInvoke::UpdateAll","shell.syncmgr_isyncmgrsynchronizeinvoke_updateall","syncmgr.isyncmgrsynchronizeinvoke_updateall"]
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke_updateall.htm
tech.root: shell
ms.assetid: 94731c78-b7cf-4ad2-afe5-6355830a5550
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeInvoke interface [Windows Shell],UpdateAll method, ISyncMgrSynchronizeInvoke.UpdateAll, ISyncMgrSynchronizeInvoke::UpdateAll, UpdateAll, UpdateAll method [Windows Shell], UpdateAll method [Windows Shell],ISyncMgrSynchronizeInvoke interface, mobsync/ISyncMgrSynchronizeInvoke::UpdateAll, shell.syncmgr_isyncmgrsynchronizeinvoke_updateall, syncmgr.isyncmgrsynchronizeinvoke_updateall
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Mobsync.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSynchronizeInvoke::UpdateAll
 - mobsync/ISyncMgrSynchronizeInvoke::UpdateAll
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeInvoke.UpdateAll
---

# ISyncMgrSynchronizeInvoke::UpdateAll


## -description

Programmatically starts an update for all items.



## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Call was completed successfully.

</td>
</tr>
</table>

## -remarks

This method returns immediately and the synchronization manager performs the synchronizations in a separate process from the calling application.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>
