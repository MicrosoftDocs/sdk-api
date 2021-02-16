---
UID: NF:shobjidl_core.ICategoryProvider.CanCategorizeOnSCID
title: ICategoryProvider::CanCategorizeOnSCID (shobjidl_core.h)
description: Determines whether a column can be used as a category.
helpviewer_keywords: ["CanCategorizeOnSCID","CanCategorizeOnSCID method [Windows Shell]","CanCategorizeOnSCID method [Windows Shell]","ICategoryProvider interface","ICategoryProvider interface [Windows Shell]","CanCategorizeOnSCID method","ICategoryProvider.CanCategorizeOnSCID","ICategoryProvider::CanCategorizeOnSCID","inet_ICategoryProvider_CanCategorizeOnSCID","shell.ICategoryProvider_CanCategorizeOnSCID","shobjidl_core/ICategoryProvider::CanCategorizeOnSCID"]
old-location: shell\ICategoryProvider_CanCategorizeOnSCID.htm
tech.root: shell
ms.assetid: e0b10007-7b25-4ddf-8cb9-76d85f8fb4df
ms.date: 12/05/2018
ms.keywords: CanCategorizeOnSCID, CanCategorizeOnSCID method [Windows Shell], CanCategorizeOnSCID method [Windows Shell],ICategoryProvider interface, ICategoryProvider interface [Windows Shell],CanCategorizeOnSCID method, ICategoryProvider.CanCategorizeOnSCID, ICategoryProvider::CanCategorizeOnSCID, inet_ICategoryProvider_CanCategorizeOnSCID, shell.ICategoryProvider_CanCategorizeOnSCID, shobjidl_core/ICategoryProvider::CanCategorizeOnSCID
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
 - ICategoryProvider::CanCategorizeOnSCID
 - shobjidl_core/ICategoryProvider::CanCategorizeOnSCID
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
 - ICategoryProvider.CanCategorizeOnSCID
---

# ICategoryProvider::CanCategorizeOnSCID


## -description

Determines whether a column can be used as a category.

## -parameters

### -param pscid [in]

Type: <b>const <a href="/windows/desktop/shell/objects">SHCOLUMNID</a>*</b>

A pointer to a <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure that identifies the column. Valid only when S_OK is returned. The GUID contained in this structure is then passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icategoryprovider-createcategory">ICategoryProvider::CreateCategory</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the column can be used as a category or S_FALSE if not.

## -remarks

When using the System Folder View Object in Category view (<b>Show in Groups</b>), the titles of columns for which this method returns S_OK appear in the upper portion of the <b>Arrange Icons By</b> submenu.