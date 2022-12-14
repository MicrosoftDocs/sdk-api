---
UID: NN:syncmgr.ISyncMgrSyncResult
title: ISyncMgrSyncResult (syncmgr.h)
description: Exposes a method that applications calling ISyncMgrControl can use to get the result of a ISyncMgrControl::StartHandlerSync or ISyncMgrControl::StartItemSync call.
helpviewer_keywords: ["ISyncMgrSyncResult","ISyncMgrSyncResult interface [Windows Shell]","ISyncMgrSyncResult interface [Windows Shell]","described","_shell_ISyncMgrSyncResult","shell.ISyncMgrSyncResult","syncmgr/ISyncMgrSyncResult"]
old-location: shell\ISyncMgrSyncResult.htm
tech.root: shell
ms.assetid: ec48eeda-5af2-4b9b-bf36-f42a6fe46fb0
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncResult, ISyncMgrSyncResult interface [Windows Shell], ISyncMgrSyncResult interface [Windows Shell],described, _shell_ISyncMgrSyncResult, shell.ISyncMgrSyncResult, syncmgr/ISyncMgrSyncResult
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
 - ISyncMgrSyncResult
 - syncmgr/ISyncMgrSyncResult
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
 - ISyncMgrSyncResult
---

# ISyncMgrSyncResult interface


## -description

Exposes a method that applications calling <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> can use to get the result of a <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">ISyncMgrControl::StartHandlerSync</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">ISyncMgrControl::StartItemSync</a> call.

## -inheritance

The <b>ISyncMgrSyncResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncResult</b> also has these types of members:

