---
UID: NF:windowsx.ListBox_GetText
title: ListBox_GetText macro
author: windows-sdk-content
description: Gets a string from a list box. You can use this macro or send the LB_GETTEXT message explicitly.
old-location: controls\ListBox_GetText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_gettext.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ListBox_GetText, ListBox_GetText macro [Windows Controls], _win32_ListBox_GetText, _win32_ListBox_GetText_cpp, controls.ListBox_GetText, controls._win32_ListBox_GetText, windowsx/ListBox_GetText
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
 - ListBox_GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_GetText macro


## -description


Gets a string from a list box.  You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761313(v=VS.85).aspx">LB_GETTEXT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


### -param lpszBuffer

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to the buffer that will receive the string. The buffer must have sufficient space for the string and a terminating null character. Before allocating the buffer, you can call <a href="https://msdn.microsoft.com/en-us/library/Bb856445(v=VS.85).aspx">ListBox_GetTextLen</a> to retrieve the length of the string. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761313(v=VS.85).aspx">LB_GETTEXT</a>.
	



