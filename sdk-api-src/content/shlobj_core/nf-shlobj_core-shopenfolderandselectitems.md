---
UID: NF:shlobj_core.SHOpenFolderAndSelectItems
title: SHOpenFolderAndSelectItems function (shlobj_core.h)
description: Opens a Windows Explorer window with specified items in a particular folder selected.
helpviewer_keywords: ["OFASI_EDIT","OFASI_OPENDESKTOP","SHOpenFolderAndSelectItems","SHOpenFolderAndSelectItems function [Windows Shell]","shell.SHOpenFolderAndSelectItems","shell_SHOpenFolderAndSelectItems","shlobj_core/SHOpenFolderAndSelectItems"]
old-location: shell\SHOpenFolderAndSelectItems.htm
tech.root: shell
ms.assetid: 1d46142d-aa4a-49fc-89dc-44266d21e405
ms.date: 12/05/2018
ms.keywords: OFASI_EDIT, OFASI_OPENDESKTOP, SHOpenFolderAndSelectItems, SHOpenFolderAndSelectItems function [Windows Shell], shell.SHOpenFolderAndSelectItems, shell_SHOpenFolderAndSelectItems, shlobj_core/SHOpenFolderAndSelectItems
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHOpenFolderAndSelectItems
 - shlobj_core/SHOpenFolderAndSelectItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHOpenFolderAndSelectItems
---

# SHOpenFolderAndSelectItems function


## -description

Opens a Windows Explorer window with specified items in a particular folder selected.

## -parameters

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to a fully qualified item ID list that specifies the folder.

### -param cidl

Type: <b>UINT</b>

A count of items in the selection array, <i>apidl</i>. If <i>cidl</i> is zero, then <i>pidlFolder</i> must point to a fully specified <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> describing a single item to select. This function opens the parent folder and selects that item.

### -param apidl [in, optional]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

A pointer to an array of PIDL structures, each of which is an item to select in the target folder referenced by <i>pidlFolder</i>.

### -param dwFlags

Type: <b>DWORD</b>

The optional flags. Under Windows XP this parameter is ignored. In Windows Vista, the following flags are defined.



#### OFASI_EDIT (0x0001)

Select an item and put its name in edit mode. This flag can only be used when a single item is being selected. For multiple item selections, it is ignored.



#### OFASI_OPENDESKTOP (0x0002)

Select the item or items on the desktop rather than in a Windows Explorer window. Note that if the desktop is obscured behind open windows, it will not be made visible.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> must be called before using <b>SHOpenFolderAndSelectItems</b>. Not doing so causes <b>SHOpenFolderAndSelectItems</b> to fail.