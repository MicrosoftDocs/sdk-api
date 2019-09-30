---
UID: NF:commctrl.ListView_SetExtendedListViewStyle
title: ListView_SetExtendedListViewStyle macro (commctrl.h)
author: windows-sdk-content
description: Sets extended styles for list-view controls. You can use this macro or send the LVM_SETEXTENDEDLISTVIEWSTYLE message explicitly.
old-location: controls\ListView_SetExtendedListViewStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setextendedlistviewstyle.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetExtendedListViewStyle, ListView_SetExtendedListViewStyle macro [Windows Controls], _win32_ListView_SetExtendedListViewStyle, _win32_ListView_SetExtendedListViewStyle_cpp, commctrl/ListView_SetExtendedListViewStyle, controls.ListView_SetExtendedListViewStyle, controls._win32_ListView_SetExtendedListViewStyle
ms.topic: macro
f1_keywords: 
 - "commctrl/ListView_SetExtendedListViewStyle"
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
 - ListView_SetExtendedListViewStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetExtendedListViewStyle macro


## -description


Sets extended styles for list-view controls. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setextendedlistviewstyle">LVM_SETEXTENDEDLISTVIEWSTYLE</a> message explicitly.


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control that will receive the style change. 


### -param dw

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A <b>DWORD</b> value that specifies the extended list-view control style. This parameter can be a combination of <a href="https://docs.microsoft.com/windows/desktop/Controls/extended-list-view-styles">Extended List-View Styles</a>. 


## -remarks



For backward compatibility reasons, the <b>ListView_SetExtendedListViewStyle</b> macro has not been updated to use 
<i>dwExMask</i>. To use the <i>dwExMask</i>value, use the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setextendedlistviewstyleex">ListView_SetExtendedListViewStyleEx</a> macro. 

When you use this macro to set the <a href="https://docs.microsoft.com/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style, any previously set state image index will be discarded. All check boxes will be initialized to the unchecked state. The state image index is contained in bits 12 through 15 of the 
<b>state</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure.



