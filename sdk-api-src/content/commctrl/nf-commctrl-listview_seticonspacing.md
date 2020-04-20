---
UID: NF:commctrl.ListView_SetIconSpacing
title: ListView_SetIconSpacing macro (commctrl.h)
description: Sets the spacing between icons in list-view controls set to the LVS_ICON style. You can use this macro or send the LVM_SETICONSPACING message explicitly.helpviewer_keywords: ["ListView_SetIconSpacing","ListView_SetIconSpacing macro [Windows Controls]","_win32_ListView_SetIconSpacing","_win32_ListView_SetIconSpacing_cpp","commctrl/ListView_SetIconSpacing","controls.ListView_SetIconSpacing","controls._win32_ListView_SetIconSpacing"]
old-location: controls\ListView_SetIconSpacing.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_seticonspacing.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetIconSpacing, ListView_SetIconSpacing macro [Windows Controls], _win32_ListView_SetIconSpacing, _win32_ListView_SetIconSpacing_cpp, commctrl/ListView_SetIconSpacing, controls.ListView_SetIconSpacing, controls._win32_ListView_SetIconSpacing
f1_keywords:
- commctrl/ListView_SetIconSpacing
dev_langs:
- c++
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
- ListView_SetIconSpacing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetIconSpacing macro


## -description


Sets the spacing between icons in list-view controls set to the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-view-window-styles">LVS_ICON</a> style. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-seticonspacing">LVM_SETICONSPACING</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param cx

Type: <b>int</b>

The distance, in pixels, to set between icons on the x-axis. 


### -param cy

Type: <b>int</b>

The distance, in pixels, to set between icons on the y-axis. 


## -remarks



The 
				<i>cx</i> and <i>cy</i> parameters are relative to the upper-left corner of an icon bitmap. Therefore, to set spacing between icons that do not overlap, the <i>cx</i> or <i>cy</i> values must include the size of the icon, plus the amount of empty space desired between icons. Values that do not include the width of the icon will result in overlaps.

When defining the icon spacing, <i>cx</i> and <i>cy</i> must set to 4 or larger. Smaller values will not yield the desired layout. You can reset <i>cx</i> and <i>cy</i> to the default spacing by setting both values to -1. This approach only allows you to reset both default settings. You cannot reset only <i>cx</i> or <i>cy</i> to the default setting by setting one of them to -1.



