---
UID: NF:syncmgr.ISyncMgrSyncCallback.ReportProgress
title: ISyncMgrSyncCallback::ReportProgress (syncmgr.h)
description: Reports the progress of the synchronization of a single sync item to Sync Center.
helpviewer_keywords: ["ISyncMgrSyncCallback interface [Windows Shell]","ReportProgress method","ISyncMgrSyncCallback.ReportProgress","ISyncMgrSyncCallback::ReportProgress","ReportProgress","ReportProgress method [Windows Shell]","ReportProgress method [Windows Shell]","ISyncMgrSyncCallback interface","_shell_ISyncMgrSyncCallback_ReportProgress","shell.ISyncMgrSyncCallback_ReportProgress","syncmgr/ISyncMgrSyncCallback::ReportProgress"]
old-location: shell\ISyncMgrSyncCallback_ReportProgress.htm
tech.root: shell
ms.assetid: fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],ReportProgress method, ISyncMgrSyncCallback.ReportProgress, ISyncMgrSyncCallback::ReportProgress, ReportProgress, ReportProgress method [Windows Shell], ReportProgress method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_ReportProgress, shell.ISyncMgrSyncCallback_ReportProgress, syncmgr/ISyncMgrSyncCallback::ReportProgress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSyncCallback::ReportProgress
 - syncmgr/ISyncMgrSyncCallback::ReportProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncCallback.ReportProgress
---

# ISyncMgrSyncCallback::ReportProgress


## -description

Reports the progress of the synchronization of a single sync item to Sync Center.

## -parameters

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item currently being synchronized. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param pszProgressText [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing a Unicode string for any custom progress messaging for this item.

### -param nStatus [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PROGRESS_STATUS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PROGRESS_STATUS</a> enumeration stating the current progress status of the synchronization.

### -param uCurrentStep [in]

Type: <b>ULONG</b>

The current step in the synchronization. If the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_UPDATING_INDETERMINATE</a> flag is set in <i>nStatus</i>, this parameter is ignored.

### -param uMaxStep [in]

Type: <b>ULONG</b>

The total number of steps required to complete the synchronization of the item. If the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_UPDATING_INDETERMINATE</a> flag is set in <i>nStatus</i>, this parameter is ignored.

### -param pnCancelRequest [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_cancel_request">SYNCMGR_CANCEL_REQUEST</a>*</b>

When this method returns, points to a value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_cancel_request">SYNCMGR_CANCEL_REQUEST</a> enumeration specifying the nature of a cancel request, if any.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you want to report progress on the handler rather than individual sync items, call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-sethandlerprogresstext">ISyncMgrSyncCallback::SetHandlerProgressText</a>.

If the synchronization has been canceled, the handler calls <b>ISyncMgrSyncCallback::ReportProgress</b> on the item one final time, acknowledging the cancellation request by specifying <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_CANCELED</a> in the <i>nStatus</i> parameter. This updates the UI and also allows the user to restart a sync for that item.

Once this method reports a completion status (<a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_SUCCEEDED</a>, <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_FAILED</a>, or <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_CANCELED</a>), the only further status report that can be made is <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PS_FAILED</a>. Any other value causes this method to return E_ACCESSDENIED and Sync Center to mark the item as failed.

This method replaces <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress">Progress</a>.

The maximum length of a progress string is MAX_SYNCMGR_PROGRESSTEXT. This constant is defined in SyncMgr.h.


#### Examples



The following example shows the usage of <b>ISyncMgrSyncCallback::ReportProgress</b> by the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a> method.


```cpp
STDMETHODIMP CMyDeviceHandler::Synchronize(...)
{
    ...

    // Start synchronizing the sync item.

    ...

    // Construct a string to display in the Sync Center folder.
    // Report the progress to Sync Center.
    SYNCMGR_CANCEL_REQUEST nCancelRequest;
    hr = pCallback->ReportProgress(pszItemID,
                                   pszProgressText,
                                   SYNCMGR_PS_UPDATING,
                                   uCurrentStep,
                                   uMaxStep,
                                   &nCancelRequest);
    if (SUCCEEDED(hr))
    {
        if (nCancelRequest != SYNCMGR_CR_NONE)
        {
            // Synchronization was canceled.
            hr = pCallback->ReportProgress(pszItemID,
                                           pszProgressText,
                                           SYNCMGR_PS_CANCELED,
                                           uCurrentStep,
                                           uMaxStep,
                                           NULL);
        }
    }
    ...
}

```