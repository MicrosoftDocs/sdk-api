---
UID: NF:shobjidl_core.IFolderView2.GetSelection
title: IFolderView2::GetSelection (shobjidl_core.h)
description: Gets the current selection as an IShellItemArray.
helpviewer_keywords: ["GetSelection","GetSelection method [Windows Shell]","GetSelection method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetSelection method","IFolderView2.GetSelection","IFolderView2::GetSelection","_shell_IFolderView2_GetSelection","shell.IFolderView2_GetSelection","shobjidl_core/IFolderView2::GetSelection"]
old-location: shell\IFolderView2_GetSelection.htm
tech.root: shell
ms.assetid: d8ff0c8f-9678-455b-b7ec-9b651df769bc
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Shell], GetSelection method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetSelection method, IFolderView2.GetSelection, IFolderView2::GetSelection, _shell_IFolderView2_GetSelection, shell.IFolderView2_GetSelection, shobjidl_core/IFolderView2::GetSelection
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
 - IFolderView2::GetSelection
 - shobjidl_core/IFolderView2::GetSelection
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
 - IFolderView2.GetSelection
---

# IFolderView2::GetSelection


## -description

Gets the current selection as an IShellItemArray.

## -parameters

### -param fNoneImpliesFolder [in]

Type: <b>BOOL</b>

If <b>TRUE</b>, this method returns an IShellItemArray containing the parent folder when there is no current selection.

### -param ppsia [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>**</b>

The address of a pointer to an IShellItemArray.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values, or an error otherwise.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The IShellItemArray returned has zero items.

</td>
</tr>
</table>