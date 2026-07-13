---
UID: NF:shobjidl_core.SHSetTemporaryPropertyForItem
title: SHSetTemporaryPropertyForItem function (shobjidl_core.h)
description: Sets a temporary property for the specified item. A temporary property is kept in a read/write store that holds properties only for the lifetime of the IShellItem object, instead of writing them back into the item.
helpviewer_keywords: ["SHSetTemporaryPropertyForItem","SHSetTemporaryPropertyForItem function [Windows Shell]","_shell_SHSetTemporaryPropertyForItem","shell.SHSetTemporaryPropertyForItem","shobjidl_core/SHSetTemporaryPropertyForItem"]
old-location: shell\SHSetTemporaryPropertyForItem.htm
tech.root: shell
ms.assetid: 779b1b2e-cd4b-404f-9d50-ac87b81640d2
ms.date: 12/05/2018
ms.keywords: SHSetTemporaryPropertyForItem, SHSetTemporaryPropertyForItem function [Windows Shell], _shell_SHSetTemporaryPropertyForItem, shell.SHSetTemporaryPropertyForItem, shobjidl_core/SHSetTemporaryPropertyForItem
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
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetTemporaryPropertyForItem
 - shobjidl_core/SHSetTemporaryPropertyForItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHSetTemporaryPropertyForItem
---

# SHSetTemporaryPropertyForItem function


## -description

Sets a temporary property for the specified item. A temporary property is kept in a read/write store that holds properties only for the lifetime of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object, instead of writing them back into the item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the item on which the temporary property is to be set.

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> that identifies the temporary property that is being set.

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> that contains the value of the temporary property.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A temporary value can only be read with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem">SHGetTemporaryPropertyForItem</a> or by passing GPS_TEMPORARY to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>.