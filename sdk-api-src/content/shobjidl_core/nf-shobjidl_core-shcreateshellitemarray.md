---
UID: NF:shobjidl_core.SHCreateShellItemArray
title: SHCreateShellItemArray function (shobjidl_core.h)
description: Creates a Shell item array object.
helpviewer_keywords: ["SHCreateShellItemArray","SHCreateShellItemArray function [Windows Shell]","_shell_SHCreateShellItemArray","shell.SHCreateShellItemArray","shobjidl_core/SHCreateShellItemArray"]
old-location: shell\SHCreateShellItemArray.htm
tech.root: shell
ms.assetid: 024ccbc7-97f1-4cb5-8588-9c9b1f747336
ms.date: 12/05/2018
ms.keywords: SHCreateShellItemArray, SHCreateShellItemArray function [Windows Shell], _shell_SHCreateShellItemArray, shell.SHCreateShellItemArray, shobjidl_core/SHCreateShellItemArray
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
 - SHCreateShellItemArray
 - shobjidl_core/SHCreateShellItemArray
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
 - SHCreateShellItemArray
---

# SHCreateShellItemArray function


## -description

Creates a Shell item array object.

## -parameters

### -param pidlParent [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The ID list of the parent folder of the items specified in <i>ppidl</i>. If <i>psf</i> is specified, this parameter can be <b>NULL</b>. If this <i>pidlParent</i> is not specified, it is computed from the <i>psf</i> parameter using <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a>.

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

The Shell data source object that is the parent of the child items specified in <i>ppidl</i>. If <i>pidlParent</i> is specified, this parameter can be <b>NULL</b>.

### -param cidl [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>ppidl</i>.

### -param ppidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

The list of child item IDs for which the array is being created. This value can be <b>NULL</b>.

### -param ppsiItemArray [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

When this function returns, contains the address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.