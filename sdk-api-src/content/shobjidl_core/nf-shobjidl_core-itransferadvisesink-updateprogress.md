---
UID: NF:shobjidl_core.ITransferAdviseSink.UpdateProgress
title: ITransferAdviseSink::UpdateProgress (shobjidl_core.h)
description: Updates the transfer progress status in the UI.
helpviewer_keywords: ["ITransferAdviseSink interface [Windows Shell]","UpdateProgress method","ITransferAdviseSink.UpdateProgress","ITransferAdviseSink::UpdateProgress","UpdateProgress","UpdateProgress method [Windows Shell]","UpdateProgress method [Windows Shell]","ITransferAdviseSink interface","_shell_ITransferAdviseSink_UpdateProgress","shell.ITransferAdviseSink_UpdateProgress","shobjidl_core/ITransferAdviseSink::UpdateProgress"]
old-location: shell\ITransferAdviseSink_UpdateProgress.htm
tech.root: shell
ms.assetid: 931029e8-48ff-4d24-8818-57b7103fffdf
ms.date: 12/05/2018
ms.keywords: ITransferAdviseSink interface [Windows Shell],UpdateProgress method, ITransferAdviseSink.UpdateProgress, ITransferAdviseSink::UpdateProgress, UpdateProgress, UpdateProgress method [Windows Shell], UpdateProgress method [Windows Shell],ITransferAdviseSink interface, _shell_ITransferAdviseSink_UpdateProgress, shell.ITransferAdviseSink_UpdateProgress, shobjidl_core/ITransferAdviseSink::UpdateProgress
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ITransferAdviseSink::UpdateProgress
 - shobjidl_core/ITransferAdviseSink::UpdateProgress
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
 - ITransferAdviseSink.UpdateProgress
---

# ITransferAdviseSink::UpdateProgress


## -description

Updates the transfer progress status in the UI.

## -parameters

### -param ullSizeCurrent [in]

Type: <b>ULONGLONG</b>

The number of bytes processed in the current operation.

### -param ullSizeTotal [in]

Type: <b>ULONGLONG</b>

The total number of bytes in the current operation.

### -param nFilesCurrent [in]

Type: <b>int</b>

The number of files processed in the current operation.

### -param nFilesTotal [in]

Type: <b>int</b>

The total number of files in the operation. Set to 0 to indicate that the value has not changed since the last call to this method.

### -param nFoldersCurrent [in]

Type: <b>int</b>

The number of folders processed in the current operation.

### -param nFoldersTotal [in]

Type: <b>int</b>

The total number of folders in the operation. Set to 0 to indicate that the value has not changed since the last call to this method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Set <i>ullSizeTotal</i>, <i>nFilesTotal</i>, and <i>nFoldersTotal</i> all to 0 to indicate that the totals have not changed since the last call to this method.

Set all six parameters to 0 to indicate that progress has not changed since the last call to this method.

<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
Implementers of this function should return an error code when the operation needs to terminate before it is complete, such as when the user clicks the <b>Cancel</b> button.

