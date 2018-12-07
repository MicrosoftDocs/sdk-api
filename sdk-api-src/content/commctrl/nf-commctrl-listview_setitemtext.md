---
UID: NF:commctrl.ListView_SetItemText
title: ListView_SetItemText macro
author: windows-sdk-content
description: Changes the text of a list-view item or subitem. You can use this macro or send the LVM_SETITEMTEXT message explicitly.
old-location: controls\ListView_SetItemText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemtext.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_SetItemText, ListView_SetItemText macro [Windows Controls], _win32_ListView_SetItemText, _win32_ListView_SetItemText_cpp, commctrl/ListView_SetItemText, controls.ListView_SetItemText, controls._win32_ListView_SetItemText
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
 - ListView_SetItemText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetItemText macro


## -description


Changes the text of a list-view item or subitem. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761198(v=VS.85).aspx">LVM_SETITEMTEXT</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The zero-based index of the list-view item. 


#### - iSubItem_

Type: <b>int</b>

The one-based index of the subitem. To set the item label, set 
					<i>iSubItem</i> to zero. 


#### - pszText_

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the new text. This parameter can be LPSTR_TEXTCALLBACK to indicate a callback item for which the parent window stores the text. In this case, the list-view control sends the parent an <a href="https://msdn.microsoft.com/en-us/library/Bb774818(v=VS.85).aspx">LVN_GETDISPINFO</a> notification code when it needs the text.
This parameter can be <b>NULL</b>.


#### - iSubItem

Type: <b>int</b>

The one-based index of the subitem. To set the item label, set 
					<i>iSubItem</i> to zero. 


#### - pszText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

A pointer to a null-terminated string that contains the new text. This parameter can be LPSTR_TEXTCALLBACK to indicate a callback item for which the parent window stores the text. In this case, the list-view control sends the parent an <a href="https://msdn.microsoft.com/en-us/library/Bb774818(v=VS.85).aspx">LVN_GETDISPINFO</a> notification code when it needs the text.
This parameter can be <b>NULL</b>.

