---
UID: NF:syncmgr.ISyncMgrHandler.Synchronize
title: ISyncMgrHandler::Synchronize (syncmgr.h)
description: Initiates a synchronization of a selection of the handler's sync items.
helpviewer_keywords: ["ISyncMgrHandler interface [Windows Shell]","Synchronize method","ISyncMgrHandler.Synchronize","ISyncMgrHandler::Synchronize","Synchronize","Synchronize method [Windows Shell]","Synchronize method [Windows Shell]","ISyncMgrHandler interface","_shell_ISyncMgrHandler_Synchronize","shell.ISyncMgrHandler_Synchronize","syncmgr/ISyncMgrHandler::Synchronize"]
old-location: shell\ISyncMgrHandler_Synchronize.htm
tech.root: shell
ms.assetid: 6742f6a8-eda8-4ef0-8a11-dc70baefcc83
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandler interface [Windows Shell],Synchronize method, ISyncMgrHandler.Synchronize, ISyncMgrHandler::Synchronize, Synchronize, Synchronize method [Windows Shell], Synchronize method [Windows Shell],ISyncMgrHandler interface, _shell_ISyncMgrHandler_Synchronize, shell.ISyncMgrHandler_Synchronize, syncmgr/ISyncMgrHandler::Synchronize
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
 - ISyncMgrHandler::Synchronize
 - syncmgr/ISyncMgrHandler::Synchronize
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
 - ISyncMgrHandler.Synchronize
---

# ISyncMgrHandler::Synchronize


## -description

Initiates a synchronization of a selection of the handler's sync items.

## -parameters

### -param ppszItemIDs [in]

Type: <b>LPCWSTR*</b>

A pointer to an array of item IDs representing the items to be synchronized. Each item ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param cItems [in]

Type: <b>ULONG</b>

The number of items in <i>ppszItemIDs</i>.

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the window that the item uses to display any necessary UI. This value can be <b>NULL</b>.

### -param pSessionCreator [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsessioncreator">ISyncMgrSessionCreator</a>*</b>

A pointer to an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsessioncreator">ISyncMgrSessionCreator</a> interface. This interface enables the handler itself to report progress and events, or to signal a background process to report progress and events.

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an interface to be passed to <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a>. <b>ISyncMgrHandler::Synchronize</b> is called either when a user requests a synchronization from the Sync Center folder or when one of the <b>ISyncMgrControl</b> synchronize methods is called, such as <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startsyncall">StartSyncAll</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ISyncMgrHandler::Synchronize</b> is called on its own thread. Sync Center instantiates the handler object and the session creator object on that thread and then calls this method. 

                

The handler can create the session itself by calling the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsessioncreator-createsession">CreateSession</a> method or it can signal an external process to perform the synchronization. If the handler creates the session, it should not return from the <b>ISyncMgrHandler::Synchronize</b> method until synchronization is complete. If the handler delegates synchronization to an external process, the external process should use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create the CLSID_SyncMgrClient object, specifying the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsessioncreator">ISyncMgrSessionCreator</a> interface. The process then creates the session so that it can report progress.

A user may elect to stop synchronization on an item or handler. An application can also stop synchronization by calling one of the stop methods on the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> interface, such as <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-stopitemsync">StopItemSync</a>. The following mechanisms are provided to support these scenarios.


<ul>
<li>
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ReportProgress</a> returns a parameter indicating whether cancellation has been requested.</li>
<li>The handler can call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-cancontinue">CanContinue</a>.</li>
</ul>


If the user asks to sync additional items after the <b>ISyncMgrHandler::Synchronize</b> method has been called, the handler can sync the new items in the same session by querying for them through the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-queryforadditionalitems">QueryForAdditionalItems</a> method on the callback. If they choose to sync an item they queried for, they can then call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-additemtosession">AddItemToSession</a>.

Some handlers will not enumerate an item until it has been synchronized. If the handler discovers such items during a synchronization, it can inform Sync Center about them through the session. For example, if the handler discovers an item to add to the sync set, it calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-proposeitem">ProposeItem</a>. Once the item has been successfully created, the handler calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-commititem">CommitItem</a>. At that point, Sync Center adds it to the list of items that it is tracking for the handler.

The <b>ISyncMgrHandler::Synchronize</b> method is analogous to a combination of the older <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">PrepareForSync</a> and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> methods. In the case of the older interface, Sync Center called <b>PrepareForSync</b> immediately followed by <b>Synchronize</b>. The <b>ISyncMgrHandler::Synchronize</b> method provides the functionality of these two methods into a single call.

                

Another difference between <b>ISyncMgrHandler::Synchronize</b> and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">Synchronize</a> is that the older method was expected to perform the synchronization asynchronously. <b>Synchronize</b> queued the request in one or more external threads and then returned. It then called <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a> once it had finished synchronizing all items. <b>ISyncMgrHandler::Synchronize</b> supports a synchronous model for in-proc (foreground) synchronization or an asynchronous model for out-of-proc (background) synchronization.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::Synchronize(__in_ecount(cItems) LPCWSTR *ppszItemIDs,
                              __in ULONG                   cItems,
                              __in HWND                    hwndOwner,
                              __in ISyncMgrSessionCreator *pCreator,
                              __in_opt IUnknown           *punk)
{
    HRESULT hr = S_OK;

    // Create the session since we are going to perform synchronization in
    // this method.
    ISyncMgrSyncCallback *pCallback = NULL;
    
    hr = pCreator->CreateSession(_szHandlerID, ppszItemIDs, cItems,&pCallback);
    if (SUCCEEDED(hr))
    {
        for (ULONG iItem = 0; iItem < cItems; iItem++)
        {
            SYNCMGR_CANCEL_REQUEST nCancelRequest = SYNCMGR_CR_NONE;
            ULONG   uCurrentStep = 1;
            ULONG   cMaxSteps    = 50;
            LPCWSTR pszItemID    = ppszItemIDs[iItem];
            WCHAR   szProgressText[256];

            // Find the item.
            CMyDeviceSyncItem *pItem = NULL;
            
            // _FindItem is a private class function that abstracts the
            // specifics of how the handler has implemented its storage of 
            // its items. Its internal details can remain transparent as 
            // they have no bearing on this example.
            hr = _FindItem(pszItemID, &pItem);
            if (FAILED(hr))
            {
                // _ReportProgress is another private class function that loads
                // string resources so that reports can be localized rather 
                // than use hard-coded strings. Its internal details have no 
                // bearing on this example.
                _ReportProgress(pCallback, 
                                pszItemID, 
                                IDS_ITEM_NOTFOUND,
                                SYNCMGR_PS_FAILED, 
                                0, 
                                0, 
                                &nCancelRequest);

                if (nCancelRequest != SYNCMGR_CR_NONE)
                {
                    break;
                }
                continue;
            }

            // Send the initial progress report to set min and max values.
            _ReportProgress(pCallback, 
                            pszItemID, 
                            IDS_START_ITEM_SYNC,
                            SYNCMGR_PS_UPDATING, 
                            uCurrentStep, 
                            cMaxSteps,
                            &nCancelRequest);

            for (; uCurrentStep < cMaxSteps; uCurrentStep++)
            {
                if (nCancelRequest != SYNCMGR_CR_NONE)
                {
                    break;
                }

                // Report progress.
                StringCchPrintfW(szProgressText, 
                                 ARRAYSIZE(szProgressText),
                                 L"Entry %d of %d", 
                                 uCurrentStep + 1, 
                                 cMaxSteps);

                pCallback->ReportProgress(pszItemID, 
                                          szProgressText,
                                          SYNCMGR_PS_UPDATING,
                                          uCurrentStep, 
                                          cMaxSteps,
                                          &nCancelRequest);

                // The code that accomplishes the synchronization goes here.
                // This code depends entirely on the nature of the items
                // involved in the sync. 
            }

            // Send the final progress report for this item.
            if (nCancelRequest != SYNCMGR_CR_NONE);
            {
                SYNCMGR_PROGRESS_STATUS nStatus = SYNCMGR_PS_SUCCEEDED;
                if (FAILED(hr))
                {
                    nStatus = SYNCMGR_PS_FAILED;
                }
                _ReportProgress(pCallback, 
                                ppszItemIDs[iItem], 
                                IDS_ITEM_SYNC_DONE,
                                nStatus, 
                                uCurrentStep - 1, 
                                cMaxSteps, 
                                &nCancelRequest);
            }

            hr = S_OK;

            if (nCancelRequest == SYNCMGR_CR_CANCEL_ALL)
            {
                 break;
            }
        }

        pCallback->Release();
    }

    return hr;
}

```