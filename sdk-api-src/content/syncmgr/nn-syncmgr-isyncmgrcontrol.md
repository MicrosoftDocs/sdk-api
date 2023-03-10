---
UID: NN:syncmgr.ISyncMgrControl
title: ISyncMgrControl (syncmgr.h)
description: Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.
helpviewer_keywords: ["ISyncMgrControl","ISyncMgrControl interface [Windows Shell]","ISyncMgrControl interface [Windows Shell]","described","_shell_ISyncMgrControl","shell.ISyncMgrControl","syncmgr/ISyncMgrControl"]
old-location: shell\ISyncMgrControl.htm
tech.root: shell
ms.assetid: 197c4e6f-ffc4-4f19-a5bd-6859eef953c2
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl, ISyncMgrControl interface [Windows Shell], ISyncMgrControl interface [Windows Shell],described, _shell_ISyncMgrControl, shell.ISyncMgrControl, syncmgr/ISyncMgrControl
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
 - ISyncMgrControl
 - syncmgr/ISyncMgrControl
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
 - ISyncMgrControl
---

# ISyncMgrControl interface


## -description

Exposes methods that allow an application or handler to start or stop a synchronization, notify Sync Center of changes to the set of handlers or items, or notify of changes to property values.

## -inheritance

The <b>ISyncMgrControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrControl</b> also has these types of members:

## -remarks

<b>ISyncMgrControl</b> is implemented by Sync Center. It can be instantiated by an application or handler as the CLSID_SyncMgrControl object, which is implemented as a Component Object Model (COM) local server. As a result, calls to <b>ISyncMgrControl</b> methods could take considerable time. Those calls should not be made on a UI thread.

All methods of this interface queue their requests with Sync Center.

<b>ISyncMgrControl</b> is a replacement for <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>.
