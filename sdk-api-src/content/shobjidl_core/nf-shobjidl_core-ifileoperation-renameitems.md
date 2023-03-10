---
UID: NF:shobjidl_core.IFileOperation.RenameItems
title: IFileOperation::RenameItems (shobjidl_core.h)
description: Declares a set of items that are to be given a new display name. All items are given the same name.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","RenameItems method","IFileOperation.RenameItems","IFileOperation::RenameItems","RenameItems","RenameItems method [Windows Shell]","RenameItems method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_RenameItems","shell.IFileOperation_RenameItems","shobjidl_core/IFileOperation::RenameItems"]
old-location: shell\IFileOperation_RenameItems.htm
tech.root: shell
ms.assetid: 325c09c6-ae32-4f5d-8b21-174dafc94aea
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],RenameItems method, IFileOperation.RenameItems, IFileOperation::RenameItems, RenameItems, RenameItems method [Windows Shell], RenameItems method [Windows Shell],IFileOperation interface, _shell_IFileOperation_RenameItems, shell.IFileOperation_RenameItems, shobjidl_core/IFileOperation::RenameItems
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
 - IFileOperation::RenameItems
 - shobjidl_core/IFileOperation::RenameItems
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
 - IFileOperation.RenameItems
---

# IFileOperation::RenameItems


## -description

Declares a set of items that are to be given a new display name. All items are given the same name.

## -parameters

### -param pUnkItems [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object which represents the group of items to be renamed. You can also point to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">IFileOperation::RenameItem</a>.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new display name of the items. This is a null-terminated, Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If more than one of the items in the collection at <i>pUnkItems</i> is in the same folder, the renamed files are appended with a number in parentheses to differentiate them, for instance newfile(1).txt, newfile(2).txt, and newfile(3).txt.

This method does not rename the items, it merely declares the items to be renamed. To rename a group of objects, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::RenameItems</b> to declare the source files or folders and the new name.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the rename operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">IFileOperation::RenameItem</a>