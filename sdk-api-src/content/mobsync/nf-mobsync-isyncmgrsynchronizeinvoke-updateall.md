---
UID: NF:mobsync.ISyncMgrSynchronizeInvoke.UpdateAll
title: ISyncMgrSynchronizeInvoke::UpdateAll (mobsync.h)
author: windows-sdk-content
description: Programmatically starts an update for all items.
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke_updateall.htm
tech.root: shell
ms.assetid: 94731c78-b7cf-4ad2-afe5-6355830a5550
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncMgrSynchronizeInvoke interface [Windows Shell],UpdateAll method, ISyncMgrSynchronizeInvoke.UpdateAll, ISyncMgrSynchronizeInvoke::UpdateAll, UpdateAll, UpdateAll method [Windows Shell], UpdateAll method [Windows Shell],ISyncMgrSynchronizeInvoke interface, mobsync/ISyncMgrSynchronizeInvoke::UpdateAll, shell.syncmgr_isyncmgrsynchronizeinvoke_updateall, syncmgr.isyncmgrsynchronizeinvoke_updateall
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeInvoke.UpdateAll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeInvoke::UpdateAll


## -description


Programmatically starts an update for all items.


## -parameters






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




<a href="https://msdn.microsoft.com/993fd482-39e0-4966-ba71-eed7e4b54f72">ISyncMgrSynchronizeInvoke</a>
 

 

