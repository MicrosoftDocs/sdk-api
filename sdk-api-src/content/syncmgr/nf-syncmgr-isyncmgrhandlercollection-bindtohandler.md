---
UID: NF:syncmgr.ISyncMgrHandlerCollection.BindToHandler
title: ISyncMgrHandlerCollection::BindToHandler (syncmgr.h)
description: Instantiates a specified sync handler when called by Sync Center.
helpviewer_keywords: ["BindToHandler","BindToHandler method [Windows Shell]","BindToHandler method [Windows Shell]","ISyncMgrHandlerCollection interface","ISyncMgrHandlerCollection interface [Windows Shell]","BindToHandler method","ISyncMgrHandlerCollection.BindToHandler","ISyncMgrHandlerCollection::BindToHandler","_shell_ISyncMgrHandlerCollection_BindToHandler","shell.ISyncMgrHandlerCollection_BindToHandler","syncmgr/ISyncMgrHandlerCollection::BindToHandler"]
old-location: shell\ISyncMgrHandlerCollection_BindToHandler.htm
tech.root: shell
ms.assetid: a3ae2427-7c7d-45b6-82ea-a8f5607f9623
ms.date: 12/05/2018
ms.keywords: BindToHandler, BindToHandler method [Windows Shell], BindToHandler method [Windows Shell],ISyncMgrHandlerCollection interface, ISyncMgrHandlerCollection interface [Windows Shell],BindToHandler method, ISyncMgrHandlerCollection.BindToHandler, ISyncMgrHandlerCollection::BindToHandler, _shell_ISyncMgrHandlerCollection_BindToHandler, shell.ISyncMgrHandlerCollection_BindToHandler, syncmgr/ISyncMgrHandlerCollection::BindToHandler
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
 - ISyncMgrHandlerCollection::BindToHandler
 - syncmgr/ISyncMgrHandlerCollection::BindToHandler
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
 - ISyncMgrHandlerCollection.BindToHandler
---

# ISyncMgrHandlerCollection::BindToHandler


## -description

Instantiates a specified sync handler when called by Sync Center.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

The ID of the sync handler.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the requested interface. This will typically be IID_ISyncMgrHandler. If the method fails when passed IID_ISyncMgrHandler, it is recalled using IID_ISyncMgrSynchronize, the IID of the older <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a> interface. When the method returns successfully, a pointer to the requested interface is referenced in the <i>ppv</i> parameter.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains an address of a pointer to an interface representing the sync handler.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is possible for this method to be called by Sync Center without it first calling <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlercollection-gethandlerenumerator">ISyncMgrHandlerCollection::GetHandlerEnumerator</a>. This is because Sync Center caches information about handlers and their items. The handler collection can return an interface pointer for an existing sync handler or it can create a new instance.

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>



<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandlercollection">ISyncMgrHandlerCollection</a>