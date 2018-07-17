---
UID: NF:commctrl.ImageList_DragLeave
title: ImageList_DragLeave function
author: windows-sdk-content
description: Unlocks the specified window and hides the drag image, allowing the window to be updated.
old-location: controls\ImageList_DragLeave.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragleave.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ImageList_DragLeave, ImageList_DragLeave function [Windows Controls], _win32_ImageList_DragLeave, _win32_ImageList_DragLeave_cpp, commctrl/ImageList_DragLeave, controls.ImageList_DragLeave, controls._win32_ImageList_DragLeave
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
 - ImageList_DragLeave
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_DragLeave function


## -description


Unlocks the specified window and hides the drag image, allowing the window to be updated. 


## -parameters




### -param hwndLock

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that owns the drag image. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 



