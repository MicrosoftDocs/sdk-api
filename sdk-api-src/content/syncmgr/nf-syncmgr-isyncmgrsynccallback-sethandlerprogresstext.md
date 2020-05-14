---
UID: NF:syncmgr.ISyncMgrSyncCallback.SetHandlerProgressText
title: ISyncMgrSyncCallback::SetHandlerProgressText (syncmgr.h)
description: Sets the content of an information field for the handler while that handler is performing a synchronization.helpviewer_keywords: ["ISyncMgrSyncCallback interface [Windows Shell]","SetHandlerProgressText method","ISyncMgrSyncCallback.SetHandlerProgressText","ISyncMgrSyncCallback::SetHandlerProgressText","SetHandlerProgressText","SetHandlerProgressText method [Windows Shell]","SetHandlerProgressText method [Windows Shell]","ISyncMgrSyncCallback interface","_shell_ISyncMgrSyncCallback_SetHandlerProgressText","shell.ISyncMgrSyncCallback_SetHandlerProgressText","syncmgr/ISyncMgrSyncCallback::SetHandlerProgressText"]
old-location: shell\ISyncMgrSyncCallback_SetHandlerProgressText.htm
tech.root: shell
ms.assetid: 5f16de5e-fed0-4d2c-a764-2239f9225cad
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],SetHandlerProgressText method, ISyncMgrSyncCallback.SetHandlerProgressText, ISyncMgrSyncCallback::SetHandlerProgressText, SetHandlerProgressText, SetHandlerProgressText method [Windows Shell], SetHandlerProgressText method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_SetHandlerProgressText, shell.ISyncMgrSyncCallback_SetHandlerProgressText, syncmgr/ISyncMgrSyncCallback::SetHandlerProgressText
f1_keywords:
- syncmgr/ISyncMgrSyncCallback.SetHandlerProgressText
dev_langs:
- c++
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
- ISyncMgrSyncCallback.SetHandlerProgressText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncCallback::SetHandlerProgressText


## -description


Sets the content of an information field for the handler while that handler is performing a synchronization.


## -parameters




### -param pszProgressText [in]

Type: <b>LPCWSTR</b>

Pointer to a buffer containing the comment text.


### -param pnCancelRequest [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_cancel_request">SYNCMGR_CANCEL_REQUEST</a>*</b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_cancel_request">SYNCMGR_CANCEL_REQUEST</a> enumeration specifying the nature of a cancel request, if any.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



