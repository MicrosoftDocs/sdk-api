---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.ShowErrorCompleted
title: ISyncMgrSynchronizeCallback::ShowErrorCompleted (mobsync.h)
description: Called by the registered application's handler before or after its PrepareForSync operation has been completed.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","ShowErrorCompleted method","ISyncMgrSynchronizeCallback.ShowErrorCompleted","ISyncMgrSynchronizeCallback::ShowErrorCompleted","ShowErrorCompleted","ShowErrorCompleted method [Windows Shell]","ShowErrorCompleted method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::ShowErrorCompleted","shell.syncmgr_isyncmgrsynchronizecallback_showerrorcompleted","syncmgr.isyncmgrsynchronizecallback_showerrorcompleted"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_showerrorcompleted.htm
tech.root: shell
ms.assetid: 7441f8d3-1b9b-400f-a2c4-ec67f7677a32
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],ShowErrorCompleted method, ISyncMgrSynchronizeCallback.ShowErrorCompleted, ISyncMgrSynchronizeCallback::ShowErrorCompleted, ShowErrorCompleted, ShowErrorCompleted method [Windows Shell], ShowErrorCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::ShowErrorCompleted, shell.syncmgr_isyncmgrsynchronizecallback_showerrorcompleted, syncmgr.isyncmgrsynchronizecallback_showerrorcompleted
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
 - ISyncMgrSynchronizeCallback::ShowErrorCompleted
 - mobsync/ISyncMgrSynchronizeCallback::ShowErrorCompleted
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
 - ISyncMgrSynchronizeCallback.ShowErrorCompleted
---

# ISyncMgrSynchronizeCallback::ShowErrorCompleted


## -description

Called by the registered application's handler before or after its <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> operation has been completed.

## -parameters

### -param hr [in]

Type: <b>HRESULT</b>

Whether <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a> was successful. This value is S_SYNCMGR_RETRYSYNC if the registered application's handler requires SyncMgr to retry the synchronization. When this value is returned to SyncMgr both the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> methods are called again.

### -param cItems [in]

Type: <b>ULONG</b>

The number of items in the array pointed to by the <i>pItemIDs</i> parameter. This parameter is ignored unless <i>hrResult</i> is S_SYNCMGR_RETRYSYNC.

### -param pItemIDs [in]

Type: <b>const GUID*</b>

A pointer to the array of item IDs to pass to 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> in the event of a retry. This parameter is ignored unless <i>hrResult</i> is S_SYNCMGR_RETRYSYNC.

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
The operation completed successfully.

</td>
</tr>
</table>

## -remarks

The <i>pItemIDs</i> parameter is an [in] parameter and the calling function owns the memory pointed to by it. SyncMgr makes a copy of the array before returning.

The registered application's handler should return from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a> method as soon as possible and then call this method to notify SyncMgr that it has completed processing the <b>ShowError</b> call.

It is acceptable for the registered application's handler to call this method 
before returning from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a> method.

The registered application's handler should not call this method unless a success code is returned from the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a> method.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ShowError</a>