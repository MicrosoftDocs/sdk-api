---
UID: NF:shobjidl_core.ICategoryProvider.EnumCategories
title: ICategoryProvider::EnumCategories (shobjidl_core.h)
description: Gets the enumerator for the list of GUIDs that represent categories.
helpviewer_keywords: ["EnumCategories","EnumCategories method [Windows Shell]","EnumCategories method [Windows Shell]","ICategoryProvider interface","ICategoryProvider interface [Windows Shell]","EnumCategories method","ICategoryProvider.EnumCategories","ICategoryProvider::EnumCategories","inet_ICategoryProvider_EnumCategories","shell.ICategoryProvider_EnumCategories","shobjidl_core/ICategoryProvider::EnumCategories"]
old-location: shell\ICategoryProvider_EnumCategories.htm
tech.root: shell
ms.assetid: 5008ce75-7a90-4f30-84e0-13d00cc1e58e
ms.date: 12/05/2018
ms.keywords: EnumCategories, EnumCategories method [Windows Shell], EnumCategories method [Windows Shell],ICategoryProvider interface, ICategoryProvider interface [Windows Shell],EnumCategories method, ICategoryProvider.EnumCategories, ICategoryProvider::EnumCategories, inet_ICategoryProvider_EnumCategories, shell.ICategoryProvider_EnumCategories, shobjidl_core/ICategoryProvider::EnumCategories
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
 - ICategoryProvider::EnumCategories
 - shobjidl_core/ICategoryProvider::EnumCategories
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
 - ICategoryProvider.EnumCategories
---

# ICategoryProvider::EnumCategories


## -description

Gets the enumerator for the list of GUIDs that represent categories.

## -parameters

### -param penum [out]

Type: <b>IEnumGUID**</b>

When this method returns, contains the address of a pointer to an <b>IEnumGUID</b> interface that specifies a list of GUIDs that represent categories.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the case of the system folder view object, <b>ICategoryProvider::EnumCategories</b> is used to obtain additional categories that are not associated with a column. When the list of category GUIDs is returned through <i>penum</i>, the UI attempts to retrieve the name of each category. That name is then displayed as a category choice. In the case of Windows XP, that choice appears in the folder's <b>Arrange Icons By</b> menu.

