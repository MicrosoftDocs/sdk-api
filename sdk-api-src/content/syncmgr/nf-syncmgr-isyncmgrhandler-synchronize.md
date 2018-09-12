---
UID: NF:syncmgr.ISyncMgrHandler.Synchronize
title: ISyncMgrHandler::Synchronize
author: windows-sdk-content
description: Initiates a synchronization of a selection of the handler's sync items.
old-location: shell\ISyncMgrHandler_Synchronize.htm
tech.root: shell
ms.assetid: 6742f6a8-eda8-4ef0-8a11-dc70baefcc83
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISyncMgrHandler interface [Windows Shell],Synchronize method, ISyncMgrHandler.Synchronize, ISyncMgrHandler::Synchronize, Synchronize, Synchronize method [Windows Shell], Synchronize method [Windows Shell],ISyncMgrHandler interface, _shell_ISyncMgrHandler_Synchronize, shell.ISyncMgrHandler_Synchronize, syncmgr/ISyncMgrHandler::Synchronize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISyncMgrHandler.Synchronize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/dc9662c5-42fa-45d2-aadd-93a5fb25d27c">ISyncMgrSessionCreator</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/dc9662c5-42fa-45d2-aadd-93a5fb25d27c">ISyncMgrSessionCreator</a> interface. This interface enables the handler itself to report progress and events, or to signal a background process to report progress and events.


### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an interface to be passed to <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a>. <b>ISyncMgrHandler::Synchronize</b> is called either when a user requests a synchronization from the Sync Center folder or when one of the <b>ISyncMgrControl</b> synchronize methods is called, such as <a href="https://msdn.microsoft.com/3b0d5070-1866-4346-b2bf-93b48a952af6">StartSyncAll</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>ISyncMgrHandler::Synchronize</b> is called on its own thread. Sync Center instantiates the handler object and the session creator object on that thread and then calls this method. 

                

The handler can create the session itself by calling the <a href="https://msdn.microsoft.com/d1df43b6-406c-4da0-89f0-a17e51101520">CreateSession</a> method or it can signal an external process to perform the synchronization. If the handler creates the session, it should not return from the <b>ISyncMgrHandler::Synchronize</b> method until synchronization is complete. If the handler delegates synchronization to an external process, the external process should use <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create the CLSID_SyncMgrClient object, specifying the <a href="https://msdn.microsoft.com/dc9662c5-42fa-45d2-aadd-93a5fb25d27c">ISyncMgrSessionCreator</a> interface. The process then creates the session so that it can report progress.

A user may elect to stop synchronization on an item or handler. An application can also stop synchronization by calling one of the stop methods on the <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> interface, such as <a href="https://msdn.microsoft.com/dd56f26b-caae-4f4d-9a32-fac450e255d0">StopItemSync</a>. The following mechanisms are provided to support these scenarios.


<ul>
<li>
<a href="https://msdn.microsoft.com/fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8">ReportProgress</a> returns a parameter indicating whether cancellation has been requested.</li>
<li>The handler can call <a href="https://msdn.microsoft.com/02106b6f-4c1c-4bd6-b120-2948b1e6d25c">CanContinue</a>.</li>
</ul>


If the user asks to sync additional items after the <b>ISyncMgrHandler::Synchronize</b> method has been called, the handler can sync the new items in the same session by querying for them through the <a href="https://msdn.microsoft.com/3780d88a-4430-4cf3-9d1c-35eb8efc8971">QueryForAdditionalItems</a> method on the callback. If they choose to sync an item they queried for, they can then call <a href="https://msdn.microsoft.com/1de3d6c0-cdf8-48fa-b7ff-2dc75f6757fc">AddItemToSession</a>.

Some handlers will not enumerate an item until it has been synchronized. If the handler discovers such items during a synchronization, it can inform Sync Center about them through the session. For example, if the handler discovers an item to add to the sync set, it calls <a href="https://msdn.microsoft.com/d0c73950-f80e-4831-9c56-4316561a269b">ProposeItem</a>. Once the item has been successfully created, the handler calls <a href="https://msdn.microsoft.com/e0964cd3-42ad-4af0-90b2-0f365f457448">CommitItem</a>. At that point, Sync Center adds it to the list of items that it is tracking for the handler.

The <b>ISyncMgrHandler::Synchronize</b> method is analogous to a combination of the older <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> and <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> methods. In the case of the older interface, Sync Center called <b>PrepareForSync</b> immediately followed by <b>Synchronize</b>. The <b>ISyncMgrHandler::Synchronize</b> method provides the functionality of these two methods into a single call.

                

Another difference between <b>ISyncMgrHandler::Synchronize</b> and <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> is that the older method was expected to perform the synchronization asynchronously. <b>Synchronize</b> queued the request in one or more external threads and then returned. It then called <a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a> once it had finished synchronizing all items. <b>ISyncMgrHandler::Synchronize</b> supports a synchronous model for in-proc (foreground) synchronization or an asynchronous model for out-of-proc (background) synchronization.


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




