---
UID: NF:shobjidl_core.IShellMenu.SetShellFolder
title: IShellMenu::SetShellFolder (shobjidl_core.h)
description: Specifies the folder for the menu band to browse.
helpviewer_keywords: ["IShellMenu interface [Windows Shell]","SetShellFolder method","IShellMenu.SetShellFolder","IShellMenu::SetShellFolder","SMSET_BOTTOM","SMSET_COLLAPSEONEMPTY","SMSET_HASEXPANDABLEFOLDERS","SMSET_USEBKICONEXTRACTION","SetShellFolder","SetShellFolder method [Windows Shell]","SetShellFolder method [Windows Shell]","IShellMenu interface","_shell_IShellMenu_SetShellFolder","shell.IShellMenu_SetShellFolder","shobjidl_core/IShellMenu::SetShellFolder"]
old-location: shell\IShellMenu_SetShellFolder.htm
tech.root: shell
ms.assetid: b442f64a-c8ab-4431-87d9-481befb51af7
ms.date: 12/05/2018
ms.keywords: IShellMenu interface [Windows Shell],SetShellFolder method, IShellMenu.SetShellFolder, IShellMenu::SetShellFolder, SMSET_BOTTOM, SMSET_COLLAPSEONEMPTY, SMSET_HASEXPANDABLEFOLDERS, SMSET_USEBKICONEXTRACTION, SetShellFolder, SetShellFolder method [Windows Shell], SetShellFolder method [Windows Shell],IShellMenu interface, _shell_IShellMenu_SetShellFolder, shell.IShellMenu_SetShellFolder, shobjidl_core/IShellMenu::SetShellFolder
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IShellMenu::SetShellFolder
 - shobjidl_core/IShellMenu::SetShellFolder
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
 - IShellMenu.SetShellFolder
---

# IShellMenu::SetShellFolder


## -description

Specifies the folder for the menu band to browse.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the folder's <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface. This pointer can be <b>NULL</b>.

### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The folder's fully qualified <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>. This value can be <b>NULL</b>.

### -param hKey [in]

Type: <b>HKEY</b>

An HKEY with an "Order" value that is used to store the order of the menu. This value can be <b>NULL</b>.

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify how the menu band operates.



#### SMSET_BOTTOM

Put this folder at the bottom of the menu.



#### SMSET_USEBKICONEXTRACTION

Use the background icon extractor.



#### SMSET_HASEXPANDABLEFOLDERS

This folder contains expandable folders.



#### SMSET_COLLAPSEONEMPTY

Collapse the menu if empty.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method after you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>.