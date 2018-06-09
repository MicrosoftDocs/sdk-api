---
UID: NS:shlobj_core._SFV_CREATE
title: "_SFV_CREATE"
author: windows-sdk-content
description: This structure is used with the SHCreateShellFolderView function.
old-location: shell\SFV_CREATE.htm
old-project: shell
ms.assetid: c6f3d9a6-5f39-4124-9340-78352f6be117
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SFV_CREATE, SFV_CREATE structure [Windows Shell], _SFV_CREATE, _win32_SFV_CREATE, shell.SFV_CREATE, shlobj_core/SFV_CREATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: SFV_CREATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SFV_CREATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _SFV_CREATE structure


## -description


This structure is used with the <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the <b>SFV_CREATE</b> structure, in bytes.


### -field pshf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

The <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface of the folder for which to create the view.


### -field psvOuter

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the parent <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface. This parameter may be <b>NULL</b>. This parameter is used only when the view created by <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> is hosted in a common dialog box.


### -field psfvcb

Type: <b><a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a> interface that handles the view's callbacks when various events occur. This parameter may be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>
 

 

