---
UID: NF:shobjidl.SHCreateDefaultPropertiesOp
title: SHCreateDefaultPropertiesOp function (shobjidl.h)
description: Creates a file operation that sets the default properties on the Shell item that have not already been set.
helpviewer_keywords: ["SHCreateDefaultPropertiesOp","SHCreateDefaultPropertiesOp function [Windows Shell]","_shell_SHCreateDefaultPropertiesOp","shell.SHCreateDefaultPropertiesOp","shobjidl/SHCreateDefaultPropertiesOp"]
old-location: shell\SHCreateDefaultPropertiesOp.htm
tech.root: shell
ms.assetid: 5202ac48-16e7-4d64-8a69-2493036e1e11
ms.date: 12/05/2018
ms.keywords: SHCreateDefaultPropertiesOp, SHCreateDefaultPropertiesOp function [Windows Shell], _shell_SHCreateDefaultPropertiesOp, shell.SHCreateDefaultPropertiesOp, shobjidl/SHCreateDefaultPropertiesOp
req.header: shobjidl.h
req.include-header: 
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
req.lib: shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateDefaultPropertiesOp
 - shobjidl/SHCreateDefaultPropertiesOp
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
 - SHCreateDefaultPropertiesOp
---

# SHCreateDefaultPropertiesOp function


## -description

Creates a file operation that sets the default properties on the Shell item that have not already been set.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the source shell item. See <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param ppFileOp [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>**</b>

The address of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The list of properties to set a default value comes from the <b>SetDefaultsFor</b> registry entry under the ProgID for the file association of the item. The list is prefixed by <code>prop:</code> and contains the canonical names of the properties to set the default value, for example, <code>prop:System.Author;System.Document.DateCreated</code>. The possible properties for this list are <a href="/windows/desktop/properties/props-system-author">System.Author</a>, <a href="/windows/desktop/properties/props-system-document-datecreated">System.Document.DateCreated</a>, and <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a>. If the <b>SetDefaultsFor</b> entry does not exist on the ProgID, this function uses the default found on the <b>SetDefaultsFor</b> entry of <b>HKEY_CLASSES_ROOT</b>&#92;<b>*</b>.