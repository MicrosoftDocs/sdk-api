---
UID: NF:shobjidl_core.IFileOperation.ApplyPropertiesToItem
title: IFileOperation::ApplyPropertiesToItem (shobjidl_core.h)
description: Declares a single item whose property values are to be set.
helpviewer_keywords: ["ApplyPropertiesToItem","ApplyPropertiesToItem method [Windows Shell]","ApplyPropertiesToItem method [Windows Shell]","IFileOperation interface","IFileOperation interface [Windows Shell]","ApplyPropertiesToItem method","IFileOperation.ApplyPropertiesToItem","IFileOperation::ApplyPropertiesToItem","_shell_IFileOperation_ApplyPropertiesToItem","shell.IFileOperation_ApplyPropertiesToItem","shobjidl_core/IFileOperation::ApplyPropertiesToItem"]
old-location: shell\IFileOperation_ApplyPropertiesToItem.htm
tech.root: shell
ms.assetid: 35330c7c-29fc-4337-a538-863925398b0d
ms.date: 12/05/2018
ms.keywords: ApplyPropertiesToItem, ApplyPropertiesToItem method [Windows Shell], ApplyPropertiesToItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],ApplyPropertiesToItem method, IFileOperation.ApplyPropertiesToItem, IFileOperation::ApplyPropertiesToItem, _shell_IFileOperation_ApplyPropertiesToItem, shell.IFileOperation_ApplyPropertiesToItem, shobjidl_core/IFileOperation::ApplyPropertiesToItem
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
 - IFileOperation::ApplyPropertiesToItem
 - shobjidl_core/IFileOperation::ApplyPropertiesToItem
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
 - IFileOperation.ApplyPropertiesToItem
---

# IFileOperation::ApplyPropertiesToItem


## -description

Declares a single item whose property values are to be set.

## -parameters

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to the item to receive the new property values.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not apply the properties to the item, it merely declares the item. To set property values on an item, you must make at least the sequence of calls detailed here:

                

<ol>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setproperties">IFileOperation::SetProperties</a> to declare the specific properties to be set and their new values.</li>
<li>Call <b>IFileOperation::ApplyPropertiesToItem</b> to declare the item whose properties are to be set.</li>
<li>Call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> to apply the properties to the item.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitems">IFileOperation::ApplyPropertiesToItems</a>