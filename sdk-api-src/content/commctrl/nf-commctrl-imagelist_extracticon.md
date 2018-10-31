---
UID: NF:commctrl.ImageList_ExtractIcon
title: ImageList_ExtractIcon macro
author: windows-sdk-content
description: Calls the ImageList_GetIcon function to create an icon or cursor based on an image and mask in an image list.
old-location: controls\ImageList_ExtractIcon.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_extracticon.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImageList_ExtractIcon, ImageList_ExtractIcon macro [Windows Controls], _win32_ImageList_ExtractIcon, _win32_ImageList_ExtractIcon_cpp, commctrl/ImageList_ExtractIcon, controls.ImageList_ExtractIcon, controls._win32_ImageList_ExtractIcon
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ImageList_ExtractIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_ExtractIcon macro


## -description


Calls the <a href="https://msdn.microsoft.com/53127531-f2ca-4f6e-a439-846db81d362e">ImageList_GetIcon</a> function to create an icon or cursor based on an image and mask in an image list. 


## -parameters




### -param hi

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

This parameter is not used and should always be zero. 


### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i

Type: <b>int</b>

The index of the image. 


## -remarks



It is the responsibility of the calling application to destroy the icon returned from this function by using the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 



