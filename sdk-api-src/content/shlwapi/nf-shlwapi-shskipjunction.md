---
UID: NF:shlwapi.SHSkipJunction
title: SHSkipJunction function (shlwapi.h)
description: Checks a bind context to see if it is safe to bind to a particular component object.
helpviewer_keywords: ["SHSkipJunction","SHSkipJunction function [Windows Shell]","_win32_SHSkipJunction","shell.SHSkipJunction","shlwapi/SHSkipJunction"]
old-location: shell\SHSkipJunction.htm
tech.root: shell
ms.assetid: 73af64a4-57eb-43db-91bb-75fe7134ad28
ms.date: 12/05/2018
ms.keywords: SHSkipJunction, SHSkipJunction function [Windows Shell], _win32_SHSkipJunction, shell.SHSkipJunction, shlwapi/SHSkipJunction
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSkipJunction
 - shlwapi/SHSkipJunction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHSkipJunction
---

# SHSkipJunction function


## -description

Checks a bind context to see if it is safe to bind to a particular component object.

## -parameters

### -param pbc [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface that specifies the bind context you want to check. This value can be <b>NULL</b>.

### -param pclsid [in]

Type: <b>const CLSID*</b>

A pointer to a variable that specifies the <b>CLSID</b> of the object being tested to see if it must be skipped. Typically, this is the CLSID of the object that <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> is about to create.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the object specified by <i>pclsid</i> must be skipped, or <b>FALSE</b> otherwise.

## -remarks

This function can be used to avoid infinite cycles in namespace binding. For example, a folder shortcut that refers to a folder above it in the namespace tree can produce an infinitely recursive loop.