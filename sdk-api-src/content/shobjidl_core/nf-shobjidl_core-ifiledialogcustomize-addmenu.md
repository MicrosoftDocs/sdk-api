---
UID: NF:shobjidl_core.IFileDialogCustomize.AddMenu
title: IFileDialogCustomize::AddMenu
author: windows-sdk-content
description: Adds a menu to the dialog.
old-location: shell\IFileDialogCustomize_AddMenu.htm
old-project: shell
ms.assetid: e5e29554-e095-4164-bf67-64f9d6a3e502
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddMenu, AddMenu method [Windows Shell], AddMenu method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddMenu method, IFileDialogCustomize.AddMenu, IFileDialogCustomize::AddMenu, shell.IFileDialogCustomize_AddMenu, shell_IFileDialogCustomize_AddMenu, shobjidl_core/IFileDialogCustomize::AddMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.AddMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::AddMenu


## -description


Adds a menu to the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the menu to add.


### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the menu name as a null-terminated Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default state for this control is enabled and visible.

To add items to this control, use <a href="https://msdn.microsoft.com/56d7d0df-0c3e-4bc3-b91e-3b191f5dad76">IFileDialogCustomize::AddControlItem</a>.



