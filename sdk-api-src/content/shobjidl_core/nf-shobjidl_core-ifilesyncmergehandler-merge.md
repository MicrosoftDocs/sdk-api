---
UID: NF:shobjidl_core.IFileSyncMergeHandler.Merge
title: IFileSyncMergeHandler::Merge (shobjidl_core.h)
description: IFileSyncMergeHandler::Merge method
helpviewer_keywords: ["IFileSyncMergeHandler interface [Windows Shell]","Merge method","IFileSyncMergeHandler.Merge","IFileSyncMergeHandler::Merge","MUS_COMPLETE","MUS_FAILED","MUS_USERINPUTNEEDED","Merge","Merge method [Windows Shell]","Merge method [Windows Shell]","IFileSyncMergeHandler interface","shell.IFileSyncMergeHandler_Merge","shobjidl_core/IFileSyncMergeHandler::Merge"]
old-location: shell\IFileSyncMergeHandler_Merge.htm
tech.root: shell
ms.assetid: 8B8410E1-0213-4647-966A-A6F9D231DCA2
ms.date: 12/05/2018
ms.keywords: IFileSyncMergeHandler interface [Windows Shell],Merge method, IFileSyncMergeHandler.Merge, IFileSyncMergeHandler::Merge, MUS_COMPLETE, MUS_FAILED, MUS_USERINPUTNEEDED, Merge, Merge method [Windows Shell], Merge method [Windows Shell],IFileSyncMergeHandler interface, shell.IFileSyncMergeHandler_Merge, shobjidl_core/IFileSyncMergeHandler::Merge
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
 - IFileSyncMergeHandler::Merge
 - shobjidl_core/IFileSyncMergeHandler::Merge
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
 - IFileSyncMergeHandler.Merge
---

# IFileSyncMergeHandler::Merge


## -description

Merges changes between the local copy and server copy of a file.

## -parameters

### -param localFilePath [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path to the local copy of the file.

### -param serverFilePath [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the network path to the server copy of the file.

### -param updateStatus [out]

Type: <b>MERGE_UPDATE_STATUS*</b>

When this method returns, contains a pointer to one of the following values indicating status of the merge process.



#### MUS_COMPLETE

Indicates that the process has completed successfully.



#### MUS_USERINPUTNEEDED

Indicates that additional input is required by the user for the process to complete.



#### MUS_FAILED

Indicates that the process has failed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler">IFileSyncMergeHandler</a>