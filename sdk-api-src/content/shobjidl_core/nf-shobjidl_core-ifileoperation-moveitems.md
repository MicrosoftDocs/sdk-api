---
UID: NF:shobjidl_core.IFileOperation.MoveItems
title: IFileOperation::MoveItems (shobjidl_core.h)
description: Declares a set of items that are to be moved to a specified destination.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","MoveItems method","IFileOperation.MoveItems","IFileOperation::MoveItems","MoveItems","MoveItems method [Windows Shell]","MoveItems method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_MoveItems","shell.IFileOperation_MoveItems","shobjidl_core/IFileOperation::MoveItems"]
old-location: shell\IFileOperation_MoveItems.htm
tech.root: shell
ms.assetid: 7b3c3fc9-5e08-44be-b0ba-a67702e2deb6
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],MoveItems method, IFileOperation.MoveItems, IFileOperation::MoveItems, MoveItems, MoveItems method [Windows Shell], MoveItems method [Windows Shell],IFileOperation interface, _shell_IFileOperation_MoveItems, shell.IFileOperation_MoveItems, shobjidl_core/IFileOperation::MoveItems
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
 - IFileOperation::MoveItems
 - shobjidl_core/IFileOperation::MoveItems
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
 - IFileOperation.MoveItems
---

# IFileOperation::MoveItems


## -description

Declares a set of items that are to be moved to a specified destination.

## -parameters

### -param punkItems [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object which represents the group of items to be moved. You can also point to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitem">IFileOperation::MoveItem</a>.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the moved items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not move the items, it merely declares the items to be moved. To move a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::MoveItems</b> to declare the source files or folders and the destination folder.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the move operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitem">IFileOperation::MoveItem</a>