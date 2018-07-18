---
UID: NF:commctrl.ImageList_DrawIndirect
title: ImageList_DrawIndirect function
author: windows-sdk-content
description: Draws an image list image based on an IMAGELISTDRAWPARAMS structure.
old-location: controls\ImageList_DrawIndirect.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_drawindirect.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ImageList_DrawIndirect, ImageList_DrawIndirect function [Windows Controls], _win32_ImageList_DrawIndirect, _win32_ImageList_DrawIndirect_cpp, commctrl/ImageList_DrawIndirect, controls.ImageList_DrawIndirect, controls._win32_ImageList_DrawIndirect
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
 - ImageList_DrawIndirect
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.70 or later)
req.irql: 
---

# ImageList_DrawIndirect function


## -description


Draws an image list image based on an <a href="https://msdn.microsoft.com/library/Bb761395(v=VS.85).aspx">IMAGELISTDRAWPARAMS</a> structure. 


## -parameters




### -param pimldp

Type: <b><a href="https://msdn.microsoft.com/library/Bb761395(v=VS.85).aspx">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Bb761395(v=VS.85).aspx">IMAGELISTDRAWPARAMS</a> structure that contains information about the draw operation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, and zero otherwise. 



