---
UID: NF:shobjidl_core.IFileOperation.MoveItem
title: IFileOperation::MoveItem (shobjidl_core.h)
description: Declares a single item that is to be moved to a specified destination.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","MoveItem method","IFileOperation.MoveItem","IFileOperation::MoveItem","MoveItem","MoveItem method [Windows Shell]","MoveItem method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_MoveItem","shell.IFileOperation_MoveItem","shobjidl_core/IFileOperation::MoveItem"]
old-location: shell\IFileOperation_MoveItem.htm
tech.root: shell
ms.assetid: 7b1e66c9-5264-42cb-9554-d1ea92625c6f
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],MoveItem method, IFileOperation.MoveItem, IFileOperation::MoveItem, MoveItem, MoveItem method [Windows Shell], MoveItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_MoveItem, shell.IFileOperation_MoveItem, shobjidl_core/IFileOperation::MoveItem
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
 - IFileOperation::MoveItem
 - shobjidl_core/IFileOperation::MoveItem
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
 - IFileOperation.MoveItem
---

# IFileOperation::MoveItem


## -description

Declares a single item that is to be moved to a specified destination.

## -parameters

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the source item.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the moved item.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item in its new location. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.

### -param pfopsItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific move operation. If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the move operation are included there, so set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not move the item, it merely declares the item to be moved. To move an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::MoveItem</b> to declare the source item, destination folder, and destination name.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the move operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitems">IFileOperation::MoveItems</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-postmoveitem">PostMoveItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-premoveitem">PreMoveItem</a>