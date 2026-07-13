---
UID: NF:shobjidl_core.IFileSyncMergeHandler.ShowResolveConflictUIAsync
title: IFileSyncMergeHandler::ShowResolveConflictUIAsync (shobjidl_core.h)
description: IFileSyncMergeHandler::ShowResolveConflictUIAsync method
helpviewer_keywords: ["IFileSyncMergeHandler interface [Windows Shell]","ShowResolveConflictUIAsync method","IFileSyncMergeHandler.ShowResolveConflictUIAsync","IFileSyncMergeHandler::ShowResolveConflictUIAsync","MUS_COMPLETE","MUS_FAILED","MUS_USERINPUTNEEDED","ShowResolveConflictUIAsync","ShowResolveConflictUIAsync method [Windows Shell]","ShowResolveConflictUIAsync method [Windows Shell]","IFileSyncMergeHandler interface","shell.IFileSyncMergeHandler_ShowResolveConflictUIAsync","shobjidl_core/IFileSyncMergeHandler::ShowResolveConflictUIAsync"]
old-location: shell\IFileSyncMergeHandler_ShowResolveConflictUIAsync.htm
tech.root: shell
ms.assetid: 7D437A9A-8F16-4E5E-B464-61A9A398C649
ms.date: 12/05/2018
ms.keywords: IFileSyncMergeHandler interface [Windows Shell],ShowResolveConflictUIAsync method, IFileSyncMergeHandler.ShowResolveConflictUIAsync, IFileSyncMergeHandler::ShowResolveConflictUIAsync, MUS_COMPLETE, MUS_FAILED, MUS_USERINPUTNEEDED, ShowResolveConflictUIAsync, ShowResolveConflictUIAsync method [Windows Shell], ShowResolveConflictUIAsync method [Windows Shell],IFileSyncMergeHandler interface, shell.IFileSyncMergeHandler_ShowResolveConflictUIAsync, shobjidl_core/IFileSyncMergeHandler::ShowResolveConflictUIAsync
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IFileSyncMergeHandler::ShowResolveConflictUIAsync
 - shobjidl_core/IFileSyncMergeHandler::ShowResolveConflictUIAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileSyncMergeHandler.ShowResolveConflictUIAsync
---

# IFileSyncMergeHandler::ShowResolveConflictUIAsync


## -description

Displays a UI to resolve conflicts between the local copy and server copy of a file.

## -parameters

### -param localFilePath [in]

Type: <b>LPCWSTR</b>

The path of the file with the merge conflict.

### -param monitorToDisplayOn [in]

Type: <b>HMONITOR</b>

Indicates the monitor on which to display the UI.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler">IFileSyncMergeHandler</a>