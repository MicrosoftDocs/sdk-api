---
UID: NF:windowsx.ListBox_Dir
title: ListBox_Dir macro
author: windows-sdk-content
description: Adds names to the list displayed by a list box.
old-location: controls\ListBox_Dir.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_dir.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListBox_Dir, ListBox_Dir macro [Windows Controls], _win32_ListBox_Dir, _win32_ListBox_Dir_cpp, controls.ListBox_Dir, controls._win32_ListBox_Dir, windowsx/ListBox_Dir
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: windowsx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_Dir
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_Dir macro


## -description


Adds names to the list displayed by a list box. The macro adds the names of directories and files that match a specified string and set of file attributes. It can also add mapped drive letters to the list box. You can use this macro or send the <a href="https://msdn.microsoft.com/5ec134e9-fe42-4cc0-bdea-fa5e66c218f6">LB_DIR</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param attrs

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The attributes of the files or directories to be added to the list box. For more information, see <a href="https://msdn.microsoft.com/5ec134e9-fe42-4cc0-bdea-fa5e66c218f6">LB_DIR</a>.


### -param lpszFileSpec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to the null-terminated string that specifies an absolute path, relative path, or filename. An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\ machinename\ sharename). 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/5ec134e9-fe42-4cc0-bdea-fa5e66c218f6">LB_DIR</a>.
	



