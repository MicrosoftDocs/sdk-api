---
UID: NF:shobjidl.IResultsFolder.RemoveItem
title: IResultsFolder::RemoveItem (shobjidl.h)
description: Removes an item from a results folder.
old-location: shell\IResultsFolder_RemoveItem.htm
tech.root: shell
ms.assetid: 17be32ed-50d7-4c16-9a06-97c4a0f8dc8d
ms.date: 12/05/2018
ms.keywords: IResultsFolder interface [Windows Shell],RemoveItem method, IResultsFolder.RemoveItem, IResultsFolder::RemoveItem, RemoveItem, RemoveItem method [Windows Shell], RemoveItem method [Windows Shell],IResultsFolder interface, _shell_IResultsFolder_RemoveItem, shell.IResultsFolder_RemoveItem, shobjidl/IResultsFolder::RemoveItem
f1_keywords:
- shobjidl/IResultsFolder.RemoveItem
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- IResultsFolder.RemoveItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResultsFolder::RemoveItem


## -description


Removes an item from a results folder.


## -parameters




### -param psi [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



