---
UID: NF:shobjidl_core.ICategoryProvider.CreateCategory
title: ICategoryProvider::CreateCategory (shobjidl_core.h)
description: Creates a category object.
helpviewer_keywords: ["CreateCategory","CreateCategory method [Windows Shell]","CreateCategory method [Windows Shell]","ICategoryProvider interface","ICategoryProvider interface [Windows Shell]","CreateCategory method","ICategoryProvider.CreateCategory","ICategoryProvider::CreateCategory","inet_ICategoryProvider_CreateCategory","shell.ICategoryProvider_CreateCategory","shobjidl_core/ICategoryProvider::CreateCategory"]
old-location: shell\ICategoryProvider_CreateCategory.htm
tech.root: shell
ms.assetid: 3703c061-4d21-4c36-900a-9ccacf4d482a
ms.date: 12/05/2018
ms.keywords: CreateCategory, CreateCategory method [Windows Shell], CreateCategory method [Windows Shell],ICategoryProvider interface, ICategoryProvider interface [Windows Shell],CreateCategory method, ICategoryProvider.CreateCategory, ICategoryProvider::CreateCategory, inet_ICategoryProvider_CreateCategory, shell.ICategoryProvider_CreateCategory, shobjidl_core/ICategoryProvider::CreateCategory
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICategoryProvider::CreateCategory
 - shobjidl_core/ICategoryProvider::CreateCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICategoryProvider.CreateCategory
---

# ICategoryProvider::CreateCategory


## -description

Creates a category object.

## -parameters

### -param pguid [in]

Type: <b>const GUID*</b>

A pointer to the <b>GUID</b> for the category object.

### -param riid [in]

Type: <b>REFIID</b>

The identifier of the object to return. Currently, the only value supported by the system folder view object is IID_ICategorizer.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the category object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

