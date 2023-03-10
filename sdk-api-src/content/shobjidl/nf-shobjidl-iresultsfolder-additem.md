---
UID: NF:shobjidl.IResultsFolder.AddItem
title: IResultsFolder::AddItem (shobjidl.h)
description: Adds an item to a results folder.
helpviewer_keywords: ["AddItem","AddItem method [Windows Shell]","AddItem method [Windows Shell]","IResultsFolder interface","IResultsFolder interface [Windows Shell]","AddItem method","IResultsFolder.AddItem","IResultsFolder::AddItem","_shell_IResultsFolder_AddItem","shell.IResultsFolder_AddItem","shobjidl/IResultsFolder::AddItem"]
old-location: shell\IResultsFolder_AddItem.htm
tech.root: shell
ms.assetid: 005f7125-8dc2-4d9c-a860-1bb56b4d0b63
ms.date: 12/05/2018
ms.keywords: AddItem, AddItem method [Windows Shell], AddItem method [Windows Shell],IResultsFolder interface, IResultsFolder interface [Windows Shell],AddItem method, IResultsFolder.AddItem, IResultsFolder::AddItem, _shell_IResultsFolder_AddItem, shell.IResultsFolder_AddItem, shobjidl/IResultsFolder::AddItem
req.header: shobjidl.h
req.include-header: 
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
 - IResultsFolder::AddItem
 - shobjidl/IResultsFolder::AddItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IResultsFolder.AddItem
---

# IResultsFolder::AddItem


## -description

Adds an item to a results folder.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.