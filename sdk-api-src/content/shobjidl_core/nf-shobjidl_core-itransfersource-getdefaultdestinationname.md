---
UID: NF:shobjidl_core.ITransferSource.GetDefaultDestinationName
title: ITransferSource::GetDefaultDestinationName (shobjidl_core.h)
description: Gets the default name for a Shell item.
helpviewer_keywords: ["GetDefaultDestinationName","GetDefaultDestinationName method [Windows Shell]","GetDefaultDestinationName method [Windows Shell]","ITransferSource interface","ITransferSource interface [Windows Shell]","GetDefaultDestinationName method","ITransferSource.GetDefaultDestinationName","ITransferSource::GetDefaultDestinationName","_shell_ITransferSource_GetDefaultDestinationName","shell.ITransferSource_GetDefaultDestinationName","shobjidl_core/ITransferSource::GetDefaultDestinationName"]
old-location: shell\ITransferSource_GetDefaultDestinationName.htm
tech.root: shell
ms.assetid: a99d9622-b205-4a8a-9840-879f655463a5
ms.date: 12/05/2018
ms.keywords: GetDefaultDestinationName, GetDefaultDestinationName method [Windows Shell], GetDefaultDestinationName method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],GetDefaultDestinationName method, ITransferSource.GetDefaultDestinationName, ITransferSource::GetDefaultDestinationName, _shell_ITransferSource_GetDefaultDestinationName, shell.ITransferSource_GetDefaultDestinationName, shobjidl_core/ITransferSource::GetDefaultDestinationName
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
 - ITransferSource::GetDefaultDestinationName
 - shobjidl_core/ITransferSource::GetDefaultDestinationName
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
 - ITransferSource.GetDefaultDestinationName
---

# ITransferSource::GetDefaultDestinationName


## -description

Gets the default name for a Shell item.

## -parameters

### -param psiSource [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param psiParentDest [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the parent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> of the destination target of the file operation.

### -param ppszDestinationName [out]

Type: <b>LPWSTR*</b>

When the method returns, contains a pointer to a null-terminated, Unicode string containing the default name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Gets the default name for a Shell item, if different than the item's parsing name.