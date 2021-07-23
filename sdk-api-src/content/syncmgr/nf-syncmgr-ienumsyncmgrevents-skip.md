---
UID: NF:syncmgr.IEnumSyncMgrEvents.Skip
title: IEnumSyncMgrEvents::Skip (syncmgr.h)
description: Skips forward the specified number of events in the enumeration.
helpviewer_keywords: ["IEnumSyncMgrEvents interface [Windows Shell]","Skip method","IEnumSyncMgrEvents.Skip","IEnumSyncMgrEvents::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","IEnumSyncMgrEvents interface","_shell_IEnumSyncMgrEvents_Skip","shell.IEnumSyncMgrEvents_Skip","syncmgr/IEnumSyncMgrEvents::Skip"]
old-location: shell\IEnumSyncMgrEvents_Skip.htm
tech.root: shell
ms.assetid: 6e8257e8-fab3-407c-a6d0-26a7a9ca0961
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrEvents interface [Windows Shell],Skip method, IEnumSyncMgrEvents.Skip, IEnumSyncMgrEvents::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumSyncMgrEvents interface, _shell_IEnumSyncMgrEvents_Skip, shell.IEnumSyncMgrEvents_Skip, syncmgr/IEnumSyncMgrEvents::Skip
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
 - IEnumSyncMgrEvents::Skip
 - syncmgr/IEnumSyncMgrEvents::Skip
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
 - IEnumSyncMgrEvents.Skip
---

# IEnumSyncMgrEvents::Skip


## -description

Skips forward the specified number of events in the enumeration.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of events to skip.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

