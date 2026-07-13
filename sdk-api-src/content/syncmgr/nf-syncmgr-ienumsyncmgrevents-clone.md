---
UID: NF:syncmgr.IEnumSyncMgrEvents.Clone
title: IEnumSyncMgrEvents::Clone (syncmgr.h)
description: Clones an IEnumSyncMgrEvents object.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumSyncMgrEvents interface","IEnumSyncMgrEvents interface [Windows Shell]","Clone method","IEnumSyncMgrEvents.Clone","IEnumSyncMgrEvents::Clone","_shell_IEnumSyncMgrEvents_Clone","shell.IEnumSyncMgrEvents_Clone","syncmgr/IEnumSyncMgrEvents::Clone"]
old-location: shell\IEnumSyncMgrEvents_Clone.htm
tech.root: shell
ms.assetid: 55be3dd4-993e-4f8f-a9d3-be5b7e4f6ddb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumSyncMgrEvents interface, IEnumSyncMgrEvents interface [Windows Shell],Clone method, IEnumSyncMgrEvents.Clone, IEnumSyncMgrEvents::Clone, _shell_IEnumSyncMgrEvents_Clone, shell.IEnumSyncMgrEvents_Clone, syncmgr/IEnumSyncMgrEvents::Clone
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
 - IEnumSyncMgrEvents::Clone
 - syncmgr/IEnumSyncMgrEvents::Clone
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
 - IEnumSyncMgrEvents.Clone
---

# IEnumSyncMgrEvents::Clone


## -description

Clones an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrevents">IEnumSyncMgrEvents</a> object.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrevents">IEnumSyncMgrEvents</a>**</b>

The address of the cloned <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrevents">IEnumSyncMgrEvents</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.