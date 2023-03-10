---
UID: NF:shlobj_core.IActiveDesktop.AddDesktopItem
title: IActiveDesktop::AddDesktopItem (shlobj_core.h)
description: Adds a desktop item.
helpviewer_keywords: ["AddDesktopItem","AddDesktopItem method [Legacy Windows Environment Features]","AddDesktopItem method [Legacy Windows Environment Features]","IActiveDesktop interface","IActiveDesktop interface [Legacy Windows Environment Features]","AddDesktopItem method","IActiveDesktop.AddDesktopItem","IActiveDesktop::AddDesktopItem","_win32_IActiveDesktop_AddDesktopItem","lwef.iactivedesktop_adddesktopitem","shell.iactivedesktop_adddesktopitem","shlobj_core/IActiveDesktop::AddDesktopItem"]
old-location: lwef\iactivedesktop_adddesktopitem.htm
tech.root: lwef
ms.assetid: 5a0c61e8-a645-4a32-b97b-8d7b43d0e5e3
ms.date: 12/05/2018
ms.keywords: AddDesktopItem, AddDesktopItem method [Legacy Windows Environment Features], AddDesktopItem method [Legacy Windows Environment Features],IActiveDesktop interface, IActiveDesktop interface [Legacy Windows Environment Features],AddDesktopItem method, IActiveDesktop.AddDesktopItem, IActiveDesktop::AddDesktopItem, _win32_IActiveDesktop_AddDesktopItem, lwef.iactivedesktop_adddesktopitem, shell.iactivedesktop_adddesktopitem, shlobj_core/IActiveDesktop::AddDesktopItem
req.header: shlobj_core.h
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
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveDesktop::AddDesktopItem
 - shlobj_core/IActiveDesktop::AddDesktopItem
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
 - IActiveDesktop.AddDesktopItem
---

# IActiveDesktop::AddDesktopItem


## -description

Adds a desktop item.

## -parameters

### -param pcomp [in]

Type: <b>LPCCOMPONENT</b>

A pointer to the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure that specifies the item to be added.

### -param dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to add the desktop item, or an instance of the desktop item already exists on the Active Desktop.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVAILDARG</b></dt>
</dl>
</td>
<td width="60%">
 One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Desktop item has been added successfully.

</td>
</tr>
</table>

## -remarks

The desktop item is added to the desktop, but it does not save it to the registry. The client application must call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges">IActiveDesktop::ApplyChanges</a> separately to update the registry.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>



<a href="/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>