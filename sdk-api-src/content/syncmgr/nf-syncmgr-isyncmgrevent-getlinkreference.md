---
UID: NF:syncmgr.ISyncMgrEvent.GetLinkReference
title: ISyncMgrEvent::GetLinkReference (syncmgr.h)
description: Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.
helpviewer_keywords: ["GetLinkReference","GetLinkReference method [Windows Shell]","GetLinkReference method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetLinkReference method","ISyncMgrEvent.GetLinkReference","ISyncMgrEvent::GetLinkReference","_shell_ISyncMgrEvent_GetLinkReference","shell.ISyncMgrEvent_GetLinkReference","syncmgr/ISyncMgrEvent::GetLinkReference"]
old-location: shell\ISyncMgrEvent_GetLinkReference.htm
tech.root: shell
ms.assetid: de625328-59ba-4574-9b7b-3e8fc643c8ad
ms.date: 12/05/2018
ms.keywords: GetLinkReference, GetLinkReference method [Windows Shell], GetLinkReference method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetLinkReference method, ISyncMgrEvent.GetLinkReference, ISyncMgrEvent::GetLinkReference, _shell_ISyncMgrEvent_GetLinkReference, shell.ISyncMgrEvent_GetLinkReference, syncmgr/ISyncMgrEvent::GetLinkReference
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
 - ISyncMgrEvent::GetLinkReference
 - syncmgr/ISyncMgrEvent::GetLinkReference
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
 - ISyncMgrEvent.GetLinkReference
---

# ISyncMgrEvent::GetLinkReference


## -description

Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.

## -parameters

### -param ppszLinkReference [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a link reference as a Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The link reference is executed when the user clicks on the hot link. When the user clicks the link, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">GetObject</a>, requesting the SYNCMGR_OBJECTID_EventLinkClick object for the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventlinkuioperation">ISyncMgrEventLinkUIOperation</a> interface. The object is initialized with an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a> interface pointer that can be used by the <i>Run</i> method. If the handler does not support this object ID, Sync Center passes the link reference to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>.
            

The event is expected to allocate the string buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.