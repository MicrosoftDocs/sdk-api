---
UID: NF:shobjidl_core.IFileOperation.RenameItem
title: IFileOperation::RenameItem (shobjidl_core.h)
description: Declares a single item that is to be given a new display name.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","RenameItem method","IFileOperation.RenameItem","IFileOperation::RenameItem","RenameItem","RenameItem method [Windows Shell]","RenameItem method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_RenameItem","shell.IFileOperation_RenameItem","shobjidl_core/IFileOperation::RenameItem"]
old-location: shell\IFileOperation_RenameItem.htm
tech.root: shell
ms.assetid: 2f72b729-3535-4ab7-9579-21b1ba97c67f
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],RenameItem method, IFileOperation.RenameItem, IFileOperation::RenameItem, RenameItem, RenameItem method [Windows Shell], RenameItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_RenameItem, shell.IFileOperation_RenameItem, shobjidl_core/IFileOperation::RenameItem
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
 - IFileOperation::RenameItem
 - shobjidl_core/IFileOperation::RenameItem
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
 - IFileOperation.RenameItem
---

# IFileOperation::RenameItem


## -description

Declares a single item that is to be given a new display name.

## -parameters

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the source item.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">display name</a> of the item. This is a null-terminated, Unicode string.

### -param pfopsItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a> object to be used for status and failure notifications. If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the rename operation are included there, so set this parameter to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not rename the item, it merely declares the item to be renamed. To rename an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::RenameItem</b> to declare the new name.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the rename operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitems">IFileOperation::RenameItems</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-postrenameitem">PostRenameItem</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-prerenameitem">PreRenameItem</a>