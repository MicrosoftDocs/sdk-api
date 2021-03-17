---
UID: NF:syncmgr.ISyncMgrSyncCallback.QueryForAdditionalItems
title: ISyncMgrSyncCallback::QueryForAdditionalItems (syncmgr.h)
description: Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized after the current synchronization is finished.
helpviewer_keywords: ["ISyncMgrSyncCallback interface [Windows Shell]","QueryForAdditionalItems method","ISyncMgrSyncCallback.QueryForAdditionalItems","ISyncMgrSyncCallback::QueryForAdditionalItems","QueryForAdditionalItems","QueryForAdditionalItems method [Windows Shell]","QueryForAdditionalItems method [Windows Shell]","ISyncMgrSyncCallback interface","_shell_ISyncMgrSyncCallback_QueryForAdditionalItems","shell.ISyncMgrSyncCallback_QueryForAdditionalItems","syncmgr/ISyncMgrSyncCallback::QueryForAdditionalItems"]
old-location: shell\ISyncMgrSyncCallback_QueryForAdditionalItems.htm
tech.root: shell
ms.assetid: 3780d88a-4430-4cf3-9d1c-35eb8efc8971
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],QueryForAdditionalItems method, ISyncMgrSyncCallback.QueryForAdditionalItems, ISyncMgrSyncCallback::QueryForAdditionalItems, QueryForAdditionalItems, QueryForAdditionalItems method [Windows Shell], QueryForAdditionalItems method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_QueryForAdditionalItems, shell.ISyncMgrSyncCallback_QueryForAdditionalItems, syncmgr/ISyncMgrSyncCallback::QueryForAdditionalItems
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
 - ISyncMgrSyncCallback::QueryForAdditionalItems
 - syncmgr/ISyncMgrSyncCallback::QueryForAdditionalItems
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
 - ISyncMgrSyncCallback.QueryForAdditionalItems
---

# ISyncMgrSyncCallback::QueryForAdditionalItems


## -description

Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized after the current synchronization is finished.

## -parameters

### -param ppenumItemIDs [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>**</b>

When this method returns, contains the address of a pointer to an instance of <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> that enumerates sync item IDs. This value is <b>NULL</b> if no items are pending.

### -param ppenumPunks [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>**</b>

When this method returns, contains the address of a pointer to an instance of <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> enumerating <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interfaces that are passed to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">StartHandlerSync</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">StartItemSync</a>. This value is <b>NULL</b> if no interfaces are pending.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise. Returns <b>S_FALSE</b> if no items are pending.

## -remarks

Item IDs retrieved by a call to the <b>Next</b> method of the retrieved enumerator interface have a maximum length of <b>MAX_SYNCMGR_ID</b> including the terminating null character. The calling application is responsible for deallocating each item ID retrieved through the <b>Next</b> method by using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.