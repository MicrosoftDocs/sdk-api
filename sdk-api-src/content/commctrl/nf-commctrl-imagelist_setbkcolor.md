---
UID: NF:commctrl.ImageList_SetBkColor
title: ImageList_SetBkColor function
author: windows-driver-content
description: Sets the background color for an image list. This function only works if you add an icon or use ImageList_AddMasked with a black and white bitmap. Without a mask, the entire image is drawn; hence the background color is not visible.
old-location: controls\ImageList_SetBkColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_setbkcolor.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ImageList_SetBkColor, ImageList_SetBkColor function [Windows Controls], _win32_ImageList_SetBkColor, _win32_ImageList_SetBkColor_cpp, commctrl/ImageList_SetBkColor, controls.ImageList_SetBkColor, controls._win32_ImageList_SetBkColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	ImageList_SetBkColor
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_SetBkColor function


## -description


Sets the background color for an image list. This function only works if you add an icon or use <a href="https://msdn.microsoft.com/ea3a3365-a453-4029-9556-f17275d373ea">ImageList_AddMasked</a> with a black and white bitmap. Without a mask, the entire image is drawn; hence the background color is not visible. 


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param clrBk [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The background color to set. This parameter can be the CLR_NONE value; in that case, images are drawn transparently using the mask. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Returns the previous background color if successful, or CLR_NONE otherwise.



