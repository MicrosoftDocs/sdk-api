---
UID: NF:commctrl.ListView_SetUnicodeFormat
title: ListView_SetUnicodeFormat macro (commctrl.h)
author: windows-sdk-content
description: Sets the Unicode character format flag for the control.
old-location: controls\ListView_SetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setunicodeformat.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_SetUnicodeFormat, ListView_SetUnicodeFormat macro [Windows Controls], _win32_ListView_SetUnicodeFormat, _win32_ListView_SetUnicodeFormat_cpp, commctrl/ListView_SetUnicodeFormat, controls.ListView_SetUnicodeFormat, controls._win32_ListView_SetUnicodeFormat
ms.topic: macro
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - ListView_SetUnicodeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetUnicodeFormat macro


## -description


Sets the Unicode character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761218(v=VS.85).aspx">LVM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

The character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775018(v=VS.85).aspx">ListView_GetUnicodeFormat</a>
 

 

