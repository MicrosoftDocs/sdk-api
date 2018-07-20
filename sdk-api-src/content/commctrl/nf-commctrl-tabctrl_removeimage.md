---
UID: NF:commctrl.TabCtrl_RemoveImage
title: TabCtrl_RemoveImage macro
author: windows-sdk-content
description: Removes an image from a tab control's image list. You can use this macro or send the TCM_REMOVEIMAGE message explicitly.
old-location: controls\TabCtrl_RemoveImage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_removeimage.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: TabCtrl_RemoveImage, TabCtrl_RemoveImage macro [Windows Controls], _win32_TabCtrl_RemoveImage, _win32_TabCtrl_RemoveImage_cpp, commctrl/TabCtrl_RemoveImage, controls.TabCtrl_RemoveImage, controls._win32_TabCtrl_RemoveImage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TabCtrl_RemoveImage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_RemoveImage macro


## -description


Removes an image from a tab control's image list. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760608(v=VS.85).aspx">TCM_REMOVEIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

TBD






#### - iImage

Type: <b>int</b>

Index of the image to remove. 


## -remarks



The tab control updates each tab's image index, so each tab remains associated with the same image as before. If a tab is using the image being removed, the tab will be set to have no image. 



