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

# ImageList_Merge function


## -description


Creates a new image by combining two existing images. The function also creates a new image list in which to store the image. 


## -parameters




### -param himl1

Type: <b>HIMAGELIST</b>

A handle to the first image list. 


### -param i1

Type: <b>int</b>

The index of the first existing image. 


### -param himl2

Type: <b>HIMAGELIST</b>

A handle to the second image list. 


### -param i2

Type: <b>int</b>

The index of the second existing image. 


### -param dx

Type: <b>int</b>

The x-offset of the second image relative to the first image. 


### -param dy

Type: <b>int</b>

The y-offset of the second image relative to the first image. 


## -returns



Type: <b>HIMAGELIST</b>

Returns the handle to the new image list if successful, or <b>NULL</b> otherwise. 




## -remarks



The new image consists of the second existing image drawn transparently over the first. The mask for the new image is the result of performing a logical OR operation on the masks of the two existing images. 



