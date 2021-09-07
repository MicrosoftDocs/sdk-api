---
UID: NF:syncmgr.IEnumSyncMgrSyncItems.Clone
title: IEnumSyncMgrSyncItems::Clone (syncmgr.h)
description: Not used. Clones an IEnumSyncMgrSyncItems object.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumSyncMgrSyncItems interface","IEnumSyncMgrSyncItems interface [Windows Shell]","Clone method","IEnumSyncMgrSyncItems.Clone","IEnumSyncMgrSyncItems::Clone","_shell_IEnumSyncMgrSyncItems_Clone","shell.IEnumSyncMgrSyncItems_Clone","syncmgr/IEnumSyncMgrSyncItems::Clone"]
old-location: shell\IEnumSyncMgrSyncItems_Clone.htm
tech.root: shell
ms.assetid: bf320918-9f63-494f-88af-a5fab91ef0e3
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumSyncMgrSyncItems interface, IEnumSyncMgrSyncItems interface [Windows Shell],Clone method, IEnumSyncMgrSyncItems.Clone, IEnumSyncMgrSyncItems::Clone, _shell_IEnumSyncMgrSyncItems_Clone, shell.IEnumSyncMgrSyncItems_Clone, syncmgr/IEnumSyncMgrSyncItems::Clone
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
 - IEnumSyncMgrSyncItems::Clone
 - syncmgr/IEnumSyncMgrSyncItems::Clone
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
 - IEnumSyncMgrSyncItems.Clone
---

# IEnumSyncMgrSyncItems::Clone


## -description

Not used. Clones an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a> object.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a>**</b>

The address of the cloned <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.