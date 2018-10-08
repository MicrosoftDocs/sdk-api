---
UID: NF:commctrl.ImageList_DragLeave
title: ImageList_DragLeave function
author: windows-sdk-content
description: Unlocks the specified window and hides the drag image, allowing the window to be updated.
old-location: controls\ImageList_DragLeave.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragleave.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ImageList_DragLeave, ImageList_DragLeave function [Windows Controls], _win32_ImageList_DragLeave, _win32_ImageList_DragLeave_cpp, commctrl/ImageList_DragLeave, controls.ImageList_DragLeave, controls._win32_ImageList_DragLeave
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ImageList_DragLeave function


## -description


Unlocks the specified window and hides the drag image, allowing the window to be updated. 


## -parameters




### -param hwndLock

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the window that owns the drag image. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 



