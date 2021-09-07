---
UID: NF:shobjidl_core.IFileOperation.DeleteItem
title: IFileOperation::DeleteItem (shobjidl_core.h)
description: Declares a single item that is to be deleted.
helpviewer_keywords: ["DeleteItem","DeleteItem method [Windows Shell]","DeleteItem method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","DeleteItem method","IFileOperation.DeleteItem","IFileOperation::DeleteItem","_shell_IFileOperation_DeleteItem","shell.IFileOperation_DeleteItem","shobjidl_core/IFileOperation::DeleteItem"]
old-location: shell\IFileOperation_DeleteItem.htm
tech.root: shell
ms.assetid: 177ce480-0309-4ec8-a6f2-0be9196bd2c8
ms.date: 12/05/2018
ms.keywords: DeleteItem, DeleteItem method [Windows Shell], DeleteItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],DeleteItem method, IFileOperation.DeleteItem, IFileOperation::DeleteItem, _shell_IFileOperation_DeleteItem, shell.IFileOperation_DeleteItem, shobjidl_core/IFileOperation::DeleteItem
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
 - IFileOperation::DeleteItem
 - shobjidl_core/IFileOperation::DeleteItem
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
 - IFileOperation.DeleteItem
---

# IFileOperation::DeleteItem


## -description

Declares a single item that is to be deleted.

## -parameters

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the item to be deleted.

### -param pfopsItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific delete operation. If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the delete operation are included there, so set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not delete the item, it merely declares the item to be deleted. To delete an item, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::DeleteItem</b> to declare the file or folder to be deleted.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the delete operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitems">IFileOperation::DeleteItems</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-postdeleteitem">PostDeleteItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-predeleteitem">PreDeleteItem</a>