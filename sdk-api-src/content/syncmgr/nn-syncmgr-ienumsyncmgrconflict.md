---
UID: NN:syncmgr.IEnumSyncMgrConflict
title: IEnumSyncMgrConflict (syncmgr.h)
description: Exposes conflict enumeration methods.
helpviewer_keywords: ["IEnumSyncMgrConflict","IEnumSyncMgrConflict interface [Windows Shell]","IEnumSyncMgrConflict interface [Windows Shell]","described","_shell_IEnumSyncMgrConflict","shell.IEnumSyncMgrConflict","syncmgr/IEnumSyncMgrConflict"]
old-location: shell\IEnumSyncMgrConflict.htm
tech.root: shell
ms.assetid: 627f39be-5c9d-49a1-af73-210cdbb7940a
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrConflict, IEnumSyncMgrConflict interface [Windows Shell], IEnumSyncMgrConflict interface [Windows Shell],described, _shell_IEnumSyncMgrConflict, shell.IEnumSyncMgrConflict, syncmgr/IEnumSyncMgrConflict
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
 - IEnumSyncMgrConflict
 - syncmgr/IEnumSyncMgrConflict
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
 - IEnumSyncMgrConflict
---

# IEnumSyncMgrConflict interface


## -description

Exposes conflict enumeration methods.

## -inheritance

The <b>IEnumSyncMgrConflict</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrConflict</b> also has these types of members:

## -remarks

A conflict store returns a pointer to an <b>IEnumSyncMgrConflict</b> interface from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrconflictstore-enumconflicts">ISyncMgrConflictStore::EnumConflicts</a>.
