---
UID: NF:shobjidl_core.ICategorizer.GetCategory
title: ICategorizer::GetCategory (shobjidl_core.h)
description: Gets a list of categories associated with a list of identifiers.
helpviewer_keywords: ["GetCategory","GetCategory method [Windows Shell]","GetCategory method [Windows Shell]","ICategorizer interface","ICategorizer interface [Windows Shell]","GetCategory method","ICategorizer.GetCategory","ICategorizer::GetCategory","inet_ICategorizer_GetCategory","shell.ICategorizer_GetCategory","shobjidl_core/ICategorizer::GetCategory"]
old-location: shell\ICategorizer_GetCategory.htm
tech.root: shell
ms.assetid: e3756e9e-7d68-4e30-92d4-1fddccf66ba5
ms.date: 12/05/2018
ms.keywords: GetCategory, GetCategory method [Windows Shell], GetCategory method [Windows Shell],ICategorizer interface, ICategorizer interface [Windows Shell],GetCategory method, ICategorizer.GetCategory, ICategorizer::GetCategory, inet_ICategorizer_GetCategory, shell.ICategorizer_GetCategory, shobjidl_core/ICategorizer::GetCategory
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
 - ICategorizer::GetCategory
 - shobjidl_core/ICategorizer::GetCategory
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
 - ICategorizer.GetCategory
---

# ICategorizer::GetCategory


## -description

Gets a list of categories associated with a list of identifiers.

## -parameters

### -param cidl [in]

Type: <b>UINT</b>

The number of items in an item identifier list array.

### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY*</b>

A pointer to an array of <i>cidl</i> item identifier list pointers.

### -param rgCategoryIds [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to an array of <i>cidl</i> category identifiers.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>ICategorizer::GetCategory</b> method accepts an array of pointers to item identifier lists (PIDLs) and fills an array of category identifiers.

<div class="alert"><b>Important</b>   The value -1 is an invalid category identifier.</div>
<div> </div>

