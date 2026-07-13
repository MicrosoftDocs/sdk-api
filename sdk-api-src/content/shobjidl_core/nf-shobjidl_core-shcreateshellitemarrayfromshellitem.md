---
UID: NF:shobjidl_core.SHCreateShellItemArrayFromShellItem
title: SHCreateShellItemArrayFromShellItem function (shobjidl_core.h)
description: Creates an array of one element from a single Shell item.
helpviewer_keywords: ["SHCreateShellItemArrayFromShellItem","SHCreateShellItemArrayFromShellItem function [Windows Shell]","_shell_SHCreateShellItemArrayFromShellItem","shell.SHCreateShellItemArrayFromShellItem","shobjidl_core/SHCreateShellItemArrayFromShellItem"]
old-location: shell\SHCreateShellItemArrayFromShellItem.htm
tech.root: shell
ms.assetid: 93401708-6f11-474d-8009-24554f316e79
ms.date: 12/05/2018
ms.keywords: SHCreateShellItemArrayFromShellItem, SHCreateShellItemArrayFromShellItem function [Windows Shell], _shell_SHCreateShellItemArrayFromShellItem, shell.SHCreateShellItemArrayFromShellItem, shobjidl_core/SHCreateShellItemArrayFromShellItem
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
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateShellItemArrayFromShellItem
 - shobjidl_core/SHCreateShellItemArrayFromShellItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHCreateShellItemArrayFromShellItem
---

# SHCreateShellItemArrayFromShellItem function


## -description

Creates an array of one element from a single Shell item.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the item.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItemArray.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically a pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a one-element array from a single item. To create an array from the contents of a folder, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray">SHCreateShellItemArray</a>.