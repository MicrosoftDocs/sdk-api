---
UID: NF:shobjidl_core.SHGetTemporaryPropertyForItem
title: SHGetTemporaryPropertyForItem function (shobjidl_core.h)
description: Retrieves the temporary property for the given item. A temporary property is a read/write store that holds properties only for the lifetime of the IShellItem object, rather than being persisted back into the item.
helpviewer_keywords: ["SHGetTemporaryPropertyForItem","SHGetTemporaryPropertyForItem function [Windows Shell]","_shell_SHGetTemporaryPropertyForItem","shell.SHGetTemporaryPropertyForItem","shobjidl_core/SHGetTemporaryPropertyForItem"]
old-location: shell\SHGetTemporaryPropertyForItem.htm
tech.root: shell
ms.assetid: 53953a5a-04a2-4749-a03b-8cbd5ac889f1
ms.date: 12/05/2018
ms.keywords: SHGetTemporaryPropertyForItem, SHGetTemporaryPropertyForItem function [Windows Shell], _shell_SHGetTemporaryPropertyForItem, shell.SHGetTemporaryPropertyForItem, shobjidl_core/SHGetTemporaryPropertyForItem
f1_keywords:
- shobjidl_core/SHGetTemporaryPropertyForItem
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- SHGetTemporaryPropertyForItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHGetTemporaryPropertyForItem function


## -description


Retrieves the temporary property for the given item. A temporary property is a read/write store that holds properties only for the lifetime of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object, rather than being persisted back into the item.


## -parameters




### -param psi [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the item for which the temporary property is to be retrieved.


### -param propkey

Type: <b>REFPROPERTYKEY</b>

The property key.


### -param ppropvar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to the temporary property for the item.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



