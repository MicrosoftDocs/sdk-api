---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.ShowPropertiesCompleted
title: ISyncMgrSynchronizeCallback::ShowPropertiesCompleted (mobsync.h)
description: Called by the registered application's handler before or after its ShowProperties operation is completed.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","ShowPropertiesCompleted method","ISyncMgrSynchronizeCallback.ShowPropertiesCompleted","ISyncMgrSynchronizeCallback::ShowPropertiesCompleted","ShowPropertiesCompleted","ShowPropertiesCompleted method [Windows Shell]","ShowPropertiesCompleted method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::ShowPropertiesCompleted","shell.syncmgr_isyncmgrsynchronizecallback_showpropertiescompleted","syncmgr.isyncmgrsynchronizecallback_showpropertiescompleted"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_showpropertiescompleted.htm
tech.root: shell
ms.assetid: d451e72e-d4a8-4899-b18e-d8912d817de5
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],ShowPropertiesCompleted method, ISyncMgrSynchronizeCallback.ShowPropertiesCompleted, ISyncMgrSynchronizeCallback::ShowPropertiesCompleted, ShowPropertiesCompleted, ShowPropertiesCompleted method [Windows Shell], ShowPropertiesCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::ShowPropertiesCompleted, shell.syncmgr_isyncmgrsynchronizecallback_showpropertiescompleted, syncmgr.isyncmgrsynchronizecallback_showpropertiescompleted
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
 - ISyncMgrSynchronizeCallback::ShowPropertiesCompleted
 - mobsync/ISyncMgrSynchronizeCallback::ShowPropertiesCompleted
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
 - ISyncMgrSynchronizeCallback.ShowPropertiesCompleted
---

# ISyncMgrSynchronizeCallback::ShowPropertiesCompleted


## -description

Called by the registered application's handler before or after its 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a> operation is completed.

## -parameters

### -param hr [in]

Type: <b>HRESULT</b>

Whether the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a> was successful.

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

It is acceptable for the registered application's handler to call this method before returning from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a> method.

This method should not be called if the registered application's handler does not return a success code from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a> method.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showproperties">ShowProperties</a>