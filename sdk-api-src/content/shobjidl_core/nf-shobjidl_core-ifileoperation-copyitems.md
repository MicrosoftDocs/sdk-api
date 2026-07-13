---
UID: NF:shobjidl_core.IFileOperation.CopyItems
title: IFileOperation::CopyItems (shobjidl_core.h)
description: Declares a set of items that are to be copied to a specified destination.
helpviewer_keywords: ["CopyItems","CopyItems method [Windows Shell]","CopyItems method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","CopyItems method","IFileOperation.CopyItems","IFileOperation::CopyItems","_shell_IFileOperation_CopyItems","shell.IFileOperation_CopyItems","shobjidl_core/IFileOperation::CopyItems"]
old-location: shell\IFileOperation_CopyItems.htm
tech.root: shell
ms.assetid: 9899cac2-bc10-422c-ab7f-2b8c1b893fc9
ms.date: 12/05/2018
ms.keywords: CopyItems, CopyItems method [Windows Shell], CopyItems method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],CopyItems method, IFileOperation.CopyItems, IFileOperation::CopyItems, _shell_IFileOperation_CopyItems, shell.IFileOperation_CopyItems, shobjidl_core/IFileOperation::CopyItems
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
 - IFileOperation::CopyItems
 - shobjidl_core/IFileOperation::CopyItems
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
 - IFileOperation.CopyItems
---

# IFileOperation::CopyItems


## -description

Declares a set of items that are to be copied to a specified destination.

## -parameters

### -param punkItems [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> object which represents the group of items to be copied. You can also point to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist">IPersistIDList</a> object to represent a single item, effectively accomplishing the same function as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">IFileOperation::CopyItem</a>.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the copy of the items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not copy the items, it merely declares the items to be copied. To copy a group of items, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::CopyItems</b> to declare the source items and the destination folder.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to begin the copy operation.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">IFileOperation::CopyItem</a>