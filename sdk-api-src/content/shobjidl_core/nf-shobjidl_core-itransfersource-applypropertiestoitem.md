---
UID: NF:shobjidl_core.ITransferSource.ApplyPropertiesToItem
title: ITransferSource::ApplyPropertiesToItem (shobjidl_core.h)
description: Apply a set of property changes to an item.
helpviewer_keywords: ["ApplyPropertiesToItem","ApplyPropertiesToItem method [Windows Shell]","ApplyPropertiesToItem method [Windows Shell]","ITransferSource interface","ITransferSource interface [Windows Shell]","ApplyPropertiesToItem method","ITransferSource.ApplyPropertiesToItem","ITransferSource::ApplyPropertiesToItem","_shell_ITransferSource_ApplyPropertiesToItem","shell.ITransferSource_ApplyPropertiesToItem","shobjidl_core/ITransferSource::ApplyPropertiesToItem"]
old-location: shell\ITransferSource_ApplyPropertiesToItem.htm
tech.root: shell
ms.assetid: f3a99637-8ce7-4177-bcf7-716ed7698934
ms.date: 12/05/2018
ms.keywords: ApplyPropertiesToItem, ApplyPropertiesToItem method [Windows Shell], ApplyPropertiesToItem method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],ApplyPropertiesToItem method, ITransferSource.ApplyPropertiesToItem, ITransferSource::ApplyPropertiesToItem, _shell_ITransferSource_ApplyPropertiesToItem, shell.ITransferSource_ApplyPropertiesToItem, shobjidl_core/ITransferSource::ApplyPropertiesToItem
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
 - ITransferSource::ApplyPropertiesToItem
 - shobjidl_core/ITransferSource::ApplyPropertiesToItem
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
 - ITransferSource.ApplyPropertiesToItem
---

# ITransferSource::ApplyPropertiesToItem


## -description

Apply a set of property changes to an item.

## -parameters

### -param psiSource [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to be altered.

### -param ppsiNew [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When this method returns, contains the address of a pointer to the changed <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.