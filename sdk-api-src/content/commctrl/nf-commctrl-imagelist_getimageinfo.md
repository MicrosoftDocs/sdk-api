---
UID: NF:commctrl.ImageList_GetImageInfo
title: ImageList_GetImageInfo function
author: windows-sdk-content
description: Retrieves information about an image.
old-location: controls\ImageList_GetImageInfo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_getimageinfo.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ImageList_GetImageInfo, ImageList_GetImageInfo function [Windows Controls], _win32_ImageList_GetImageInfo, _win32_ImageList_GetImageInfo_cpp, commctrl/ImageList_GetImageInfo, controls.ImageList_GetImageInfo, controls._win32_ImageList_GetImageInfo
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
 - ImageList_GetImageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_GetImageInfo function


## -description


Retrieves information about an image. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i

Type: <b>int</b>

The index of the image. 


### -param pImageInfo

Type: <b><a href="https://msdn.microsoft.com/1f02cff9-1381-4396-a5fa-64960e5d9a99">IMAGEINFO</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/1f02cff9-1381-4396-a5fa-64960e5d9a99">IMAGEINFO</a> structure that receives information about the image. The information in this structure can be used to directly manipulate the bitmaps for the image. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



An application should not call <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> to destroy the bitmaps retrieved by <b>ImageList_GetImageInfo</b>. The system destroys the bitmaps when the application calls the <a href="https://msdn.microsoft.com/6720c9e7-b35f-4acd-8fa7-9aa9f0991879">ImageList_Destroy</a> function. 



