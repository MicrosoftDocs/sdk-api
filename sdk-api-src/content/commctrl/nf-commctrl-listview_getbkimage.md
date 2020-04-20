---
UID: NF:commctrl.ListView_GetBkImage
title: ListView_GetBkImage macro (commctrl.h)
description: Gets the background image in a list-view control. You can use this macro or send the LVM_GETBKIMAGE message explicitly.helpviewer_keywords: ["ListView_GetBkImage","ListView_GetBkImage macro [Windows Controls]","_win32_ListView_GetBkImage","_win32_ListView_GetBkImage_cpp","commctrl/ListView_GetBkImage","controls.ListView_GetBkImage","controls._win32_ListView_GetBkImage"]
old-location: controls\ListView_GetBkImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getbkimage.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetBkImage, ListView_GetBkImage macro [Windows Controls], _win32_ListView_GetBkImage, _win32_ListView_GetBkImage_cpp, commctrl/ListView_GetBkImage, controls.ListView_GetBkImage, controls._win32_ListView_GetBkImage
f1_keywords:
- commctrl/ListView_GetBkImage
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
- ListView_GetBkImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetBkImage macro


## -description


Gets the background image in a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getbkimage">LVM_GETBKIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvbkimagea">LVBKIMAGE</a> structure that will receive the background image information. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-listview_setbkimage">ListView_SetBkImage</a>
 

 

