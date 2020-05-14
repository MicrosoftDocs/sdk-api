---
UID: NF:commctrl.Header_SetImageList
title: Header_SetImageList macro (commctrl.h)
description: Assigns an image list to an existing header control. You can use this macro or send the HDM_SETIMAGELIST message explicitly.helpviewer_keywords: ["Header_SetImageList","Header_SetImageList macro [Windows Controls]","_win32_Header_SetImageList","_win32_Header_SetImageList_cpp","commctrl/Header_SetImageList","controls.Header_SetImageList","controls._win32_Header_SetImageList"]
old-location: controls\Header_SetImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setimagelist.htm
ms.date: 12/05/2018
ms.keywords: Header_SetImageList, Header_SetImageList macro [Windows Controls], _win32_Header_SetImageList, _win32_Header_SetImageList_cpp, commctrl/Header_SetImageList, controls.Header_SetImageList, controls._win32_Header_SetImageList
f1_keywords:
- commctrl/Header_SetImageList
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
- Header_SetImageList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_SetImageList macro


## -description


Assigns an image list to an existing header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-setimagelist">HDM_SETIMAGELIST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control. 


### -param himl

Type: <b>HIMAGELIST</b>

A handle to an image list. 

