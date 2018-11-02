---
UID: NF:commctrl.ImageList_SetImageCount
title: ImageList_SetImageCount function
author: windows-sdk-content
description: Resizes an existing image list.
old-location: controls\ImageList_SetImageCount.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_setimagecount.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImageList_SetImageCount, ImageList_SetImageCount function [Windows Controls], _win32_ImageList_SetImageCount, _win32_ImageList_SetImageCount_cpp, commctrl/ImageList_SetImageCount, controls.ImageList_SetImageCount, controls._win32_ImageList_SetImageCount
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
 - ImageList_SetImageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_SetImageCount function


## -description


Resizes an existing image list. 


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list that will be resized. 


### -param uNewCount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A value specifying the new size of the image list. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



If an application expands an image list with this function, it must add new images by using the <a href="https://msdn.microsoft.com/en-us/library/Bb775213(v=VS.85).aspx">ImageList_Replace</a> function. If your application does not add valid images at the new indexes, draw operations that use the new indexes will be unpredictable. 

If you decrease the size of an image list by using this function, the truncated images are freed.



