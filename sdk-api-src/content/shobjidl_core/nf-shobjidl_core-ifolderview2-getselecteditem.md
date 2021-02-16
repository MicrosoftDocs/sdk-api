---
UID: NF:shobjidl_core.IFolderView2.GetSelectedItem
title: IFolderView2::GetSelectedItem (shobjidl_core.h)
description: Locates the currently selected item at or after a given index.
helpviewer_keywords: ["GetSelectedItem","GetSelectedItem method [Windows Shell]","GetSelectedItem method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetSelectedItem method","IFolderView2.GetSelectedItem","IFolderView2::GetSelectedItem","_shell_IFolderView2_GetSelectedItem","shell.IFolderView2_GetSelectedItem","shobjidl_core/IFolderView2::GetSelectedItem"]
old-location: shell\IFolderView2_GetSelectedItem.htm
tech.root: shell
ms.assetid: fca9fd45-05ce-4300-aecf-a2843614a11d
ms.date: 12/05/2018
ms.keywords: GetSelectedItem, GetSelectedItem method [Windows Shell], GetSelectedItem method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetSelectedItem method, IFolderView2.GetSelectedItem, IFolderView2::GetSelectedItem, _shell_IFolderView2_GetSelectedItem, shell.IFolderView2_GetSelectedItem, shobjidl_core/IFolderView2::GetSelectedItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderView2::GetSelectedItem
 - shobjidl_core/IFolderView2::GetSelectedItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.GetSelectedItem
---

# IFolderView2::GetSelectedItem


## -description

Locates the currently selected item at or after a given index.

## -parameters

### -param iStart [in]

Type: <b>int</b>

The index position from which to start searching for the currently selected item.

### -param piItem [out]

Type: <b>int*</b>

A pointer to a value that receives the index of the item in the view.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if a selected item was found, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Item not found. Note that this is a success code. The operation was successful in searching the view, it simply did not find a currently selected item after the given index (<i>iStart</i>). It is possible that no item was selected, or that the selected item had an index less than <i>iStart</i>.

</td>
</tr>
</table>

