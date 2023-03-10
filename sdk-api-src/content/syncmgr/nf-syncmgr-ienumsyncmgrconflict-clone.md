---
UID: NF:syncmgr.IEnumSyncMgrConflict.Clone
title: IEnumSyncMgrConflict::Clone (syncmgr.h)
description: Not used. Clones an IEnumSyncMgrConflict object.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumSyncMgrConflict interface","IEnumSyncMgrConflict interface [Windows Shell]","Clone method","IEnumSyncMgrConflict.Clone","IEnumSyncMgrConflict::Clone","_shell_IEnumSyncMgrConflict_Clone","shell.IEnumSyncMgrConflict_Clone","syncmgr/IEnumSyncMgrConflict::Clone"]
old-location: shell\IEnumSyncMgrConflict_Clone.htm
tech.root: shell
ms.assetid: 2eb0f1c1-71e2-45e6-bef7-1b480efb4ab7
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumSyncMgrConflict interface, IEnumSyncMgrConflict interface [Windows Shell],Clone method, IEnumSyncMgrConflict.Clone, IEnumSyncMgrConflict::Clone, _shell_IEnumSyncMgrConflict_Clone, shell.IEnumSyncMgrConflict_Clone, syncmgr/IEnumSyncMgrConflict::Clone
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
 - IEnumSyncMgrConflict::Clone
 - syncmgr/IEnumSyncMgrConflict::Clone
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
 - IEnumSyncMgrConflict.Clone
---

# IEnumSyncMgrConflict::Clone


## -description

Not used. Clones an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrconflict">IEnumSyncMgrConflict</a> object.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrconflict">IEnumSyncMgrConflict</a>**</b>

The address of the cloned <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrconflict">IEnumSyncMgrConflict</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.