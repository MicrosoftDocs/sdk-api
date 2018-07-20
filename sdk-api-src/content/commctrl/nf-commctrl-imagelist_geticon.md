---
UID: NF:commctrl.ImageList_GetIcon
title: ImageList_GetIcon function
author: windows-sdk-content
description: Creates an icon from an image and mask in an image list.
old-location: controls\ImageList_GetIcon.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_geticon.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ImageList_GetIcon, ImageList_GetIcon function [Windows Controls], _win32_ImageList_GetIcon, _win32_ImageList_GetIcon_cpp, commctrl/ImageList_GetIcon, controls.ImageList_GetIcon, controls._win32_ImageList_GetIcon
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_GetIcon
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_GetIcon function


## -description


Creates an icon from an image and mask in an image list. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i

Type: <b>int</b>

An index of the image. 


### -param flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of flags that specify the drawing style. For a list of values, see the description of the <i>fStyle</i> parameter of the <a href="https://msdn.microsoft.com/library/Bb761533(v=VS.85).aspx">ImageList_Draw</a> function. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a></b>

Returns the handle to the icon if successful, or <b>NULL</b> otherwise. 




## -remarks



It is the responsibility of the calling application to destroy the icon returned from this function using the <a href="https://msdn.microsoft.com/library/ms648063(v=VS.85).aspx">DestroyIcon</a> function. 



