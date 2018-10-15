---
UID: NF:commctrl.ListView_GetStringWidth
title: ListView_GetStringWidth macro
author: windows-sdk-content
description: Determines the width of a specified string using the specified list-view control's current font. You can use this macro or send the LVM_GETSTRINGWIDTH message explicitly.
old-location: controls\ListView_GetStringWidth.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getstringwidth.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ListView_GetStringWidth, ListView_GetStringWidth macro [Windows Controls], _win32_ListView_GetStringWidth, _win32_ListView_GetStringWidth_cpp, commctrl/ListView_GetStringWidth, controls.ListView_GetStringWidth, controls._win32_ListView_GetStringWidth
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ListView_GetStringWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetStringWidth macro


## -description


Determines the width of a specified string using the specified list-view control's current font. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761073(v=VS.85).aspx">LVM_GETSTRINGWIDTH</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param psz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A pointer to a null-terminated string. 


## -remarks



The <b>ListView_GetStringWidth</b> macro returns the exact width, in pixels, of the specified string. If you use the returned string width as the column width in a call to the <a href="https://msdn.microsoft.com/en-us/library/Bb775074(v=VS.85).aspx">ListView_SetColumnWidth</a> macro, the string will be truncated. To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width. 



