---
UID: NF:windowsx.ComboBox_Dir
title: ComboBox_Dir macro
author: windows-sdk-content
description: Adds names to the list displayed by a combo box.
old-location: controls\ComboBox_Dir.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_dir.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ComboBox_Dir, ComboBox_Dir macro [Windows Controls], _win32_ComboBox_Dir, _win32_ComboBox_Dir_cpp, controls.ComboBox_Dir, controls._win32_ComboBox_Dir, windowsx/ComboBox_Dir
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ComboBox_Dir
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_Dir macro


## -description


Adds names to the list displayed by a combo box. The macro adds the names of directories and files that match a specified string and set of file attributes. It can also add mapped drive letters to the list in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775832(v=VS.85).aspx">CB_DIR</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param attrs

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The attributes of the files or directories to be added to the list in a combo box. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775832(v=VS.85).aspx">CB_DIR</a>.


### -param lpszFileSpec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to the null-terminated string that specifies an absolute path, relative path, or filename. An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\ machinename\ sharename). 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775832(v=VS.85).aspx">CB_DIR</a>.
	



