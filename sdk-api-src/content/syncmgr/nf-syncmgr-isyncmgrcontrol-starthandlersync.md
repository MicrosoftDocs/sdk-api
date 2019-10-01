---
UID: NF:syncmgr.ISyncMgrControl.StartHandlerSync
title: ISyncMgrControl::StartHandlerSync (syncmgr.h)
author: windows-sdk-content
description: Initiates the synchronization of all items managed by a particular handler.
old-location: shell\ISyncMgrControl_StartHandlerSync.htm
tech.root: shell
ms.assetid: ab0e6634-d30a-4f56-94ff-3b032c789cec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],StartHandlerSync method, ISyncMgrControl.StartHandlerSync, ISyncMgrControl::StartHandlerSync, StartHandlerSync, StartHandlerSync method [Windows Shell], StartHandlerSync method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_StartHandlerSync, shell.ISyncMgrControl_StartHandlerSync, syncmgr/ISyncMgrControl::StartHandlerSync
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrControl.StartHandlerSync"
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - ISyncMgrControl.StartHandlerSync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrControl::StartHandlerSync


## -description


Initiates the synchronization of all items managed by a particular handler.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler to synchronize. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the window that the handler can use to display any necessary UI. This value can be <b>NULL</b>.


### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> to be passed to <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a>. This parameter can be <b>NULL</b>.


### -param nSyncControlFlags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_sync_control_flags">SYNCMGR_SYNC_CONTROL_FLAGS</a></b>

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_sync_control_flags">SYNCMGR_SYNC_CONTROL_FLAGS</a> enumeration that specifies whether an item found in both a current sync and a queued sync should be synchronized again when the queued sync is performed.


### -param pResult [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncresult">ISyncMgrSyncResult</a>*</b>

A pointer to an instance of <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncresult">ISyncMgrSyncResult</a>, whose <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncresult-result">Result</a> method is called when the synchronization ends, either through success, failure, or cancellation. The <b>Result</b> method is called with the aggregated state of the handler synchronization. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



