---
UID: NF:commctrl.TabCtrl_RemoveImage
title: TabCtrl_RemoveImage macro (commctrl.h)
description: Removes an image from a tab control's image list. You can use this macro or send the TCM_REMOVEIMAGE message explicitly.
helpviewer_keywords: ["TabCtrl_RemoveImage","TabCtrl_RemoveImage macro [Windows Controls]","_win32_TabCtrl_RemoveImage","_win32_TabCtrl_RemoveImage_cpp","commctrl/TabCtrl_RemoveImage","controls.TabCtrl_RemoveImage","controls._win32_TabCtrl_RemoveImage"]
old-location: controls\TabCtrl_RemoveImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_removeimage.htm
ms.date: 12/05/2018
ms.keywords: TabCtrl_RemoveImage, TabCtrl_RemoveImage macro [Windows Controls], _win32_TabCtrl_RemoveImage, _win32_TabCtrl_RemoveImage_cpp, commctrl/TabCtrl_RemoveImage, controls.TabCtrl_RemoveImage, controls._win32_TabCtrl_RemoveImage
f1_keywords:
- commctrl/TabCtrl_RemoveImage
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
- TabCtrl_RemoveImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TabCtrl_RemoveImage macro


## -description


Removes an image from a tab control's image list. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/tcm-removeimage">TCM_REMOVEIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tab control. 


### -param i

Type: <b>int</b>

Index of the image to remove. 


## -remarks



The tab control updates each tab's image index, so each tab remains associated with the same image as before. If a tab is using the image being removed, the tab will be set to have no image. 



