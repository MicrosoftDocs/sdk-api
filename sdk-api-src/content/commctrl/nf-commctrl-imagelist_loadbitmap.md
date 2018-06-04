---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ImageList_LoadBitmap macro


## -description


Calls the <a href="https://msdn.microsoft.com/6392e485-10f4-46c1-a089-f447d078a20e">ImageList_LoadImage</a> function to create an image list from the specified bitmap resource. 


## -parameters




### -param hi

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

A handle to the instance that contains the bitmap resource. This parameter is <b>NULL</b> if you are loading an OEM bitmap. 


### -param lpbmp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The image to load. If the <i>hi</i> parameter is non-<b>NULL</b>, <i>lpbmp</i>is the address of a null-terminated string that contains the name of the image resource in the <i>hi</i> module. If <i>hi</i> is <b>NULL</b>, the <a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a> of this parameter must be the identifier of an OEM bitmap to load. To create this value, use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro with one of the OEM bitmap identifiers defined in WINUSER.H. These identifiers have the OBM_ prefix.


### -param cx

Type: <b>int</b>

The width of each image. The height of each image and the initial number of images are inferred by the dimensions of the specified bitmap. 


### -param cGrow

Type: <b>int</b>

The number of images by which the image list can grow when the system needs to make room for new images. This parameter represents the number of new images that the resized image list can contain.


### -param crMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The color used to generate a mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is the CLR_NONE value, no mask is generated. 

