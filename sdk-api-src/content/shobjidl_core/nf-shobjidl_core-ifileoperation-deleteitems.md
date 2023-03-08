---
UID: NF:shobjidl_core.IFileOperation.DeleteItems
title: IFileOperation::DeleteItems (shobjidl_core.h)
description: Declares a set of items that are to be deleted.
helpviewer_keywords: ["DeleteItems","DeleteItems method [Windows Shell]","DeleteItems method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","DeleteItems method","IFileOperation.DeleteItems","IFileOperation::DeleteItems","_shell_IFileOperation_DeleteItems","shell.IFileOperation_DeleteItems","shobjidl_core/IFileOperation::DeleteItems"]
old-location: shell\IFileOperation_DeleteItems.htm
tech.root: shell
ms.assetid: 708072c4-c0c7-4d7d-a54f-234c57ff08e6
ms.date: 12/05/2018
ms.keywords: DeleteItems, DeleteItems method [Windows Shell], DeleteItems method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],DeleteItems method, IFileOperation.DeleteItems, IFileOperation::DeleteItems, _shell_IFileOperation_DeleteItems, shell.IFileOperation_DeleteItems, shobjidl_core/IFileOperation::DeleteItems
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
 - IFileOperation::DeleteItems
 - shobjidl_core/IFileOperation::DeleteItems
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
 - IFileOperation.DeleteItems
---

# IFileOperation::DeleteItems


## -description

Declares a set of items that are to be deleted.

## -parameters

### -param punkItems [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object which represents the group of items to be deleted. You can also point to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">IFileOperation::DeleteItem</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not delete the items, it merely declares the items to be deleted. To delete a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::DeleteItems</b> to declare the files or folders to be deleted.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the delete operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">IFileOperation::DeleteItem</a>