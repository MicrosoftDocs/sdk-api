---
UID: NF:syncmgr.ISyncMgrSyncCallback.QueryForAdditionalItems
title: ISyncMgrSyncCallback::QueryForAdditionalItems
author: windows-sdk-content
description: Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized after the current synchronization is finished.
old-location: shell\ISyncMgrSyncCallback_QueryForAdditionalItems.htm
old-project: shell
ms.assetid: 3780d88a-4430-4cf3-9d1c-35eb8efc8971
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],QueryForAdditionalItems method, ISyncMgrSyncCallback.QueryForAdditionalItems, ISyncMgrSyncCallback::QueryForAdditionalItems, QueryForAdditionalItems, QueryForAdditionalItems method [Windows Shell], QueryForAdditionalItems method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_QueryForAdditionalItems, shell.ISyncMgrSyncCallback_QueryForAdditionalItems, syncmgr/ISyncMgrSyncCallback::QueryForAdditionalItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncCallback.QueryForAdditionalItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncCallback::QueryForAdditionalItems


## -description


Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized after the current synchronization is finished.


## -parameters




### -param ppenumItemIDs [out]

Type: <b><a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>**</b>

When this method returns, contains the address of a pointer to an instance of <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> that enumerates sync item IDs. This value is <b>NULL</b> if no items are pending.


### -param ppenumPunks [out]

Type: <b><a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>**</b>

When this method returns, contains the address of a pointer to an instance of <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> enumerating <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interfaces that are passed to <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">StartHandlerSync</a> or <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">StartItemSync</a>. This value is <b>NULL</b> if no interfaces are pending.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise. Returns <b>S_FALSE</b> if no items are pending.




## -remarks



Item IDs retrieved by a call to the <b>Next</b> method of the retrieved enumerator interface have a maximum length of <b>MAX_SYNCMGR_ID</b> including the terminating null character. The calling application is responsible for deallocating each item ID retrieved through the <b>Next</b> method by using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.



