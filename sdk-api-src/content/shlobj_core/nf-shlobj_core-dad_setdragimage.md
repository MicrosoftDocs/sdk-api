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

# DAD_SetDragImage function


## -description


<p class="CCE_Message">[<b>DAD_SetDragImage</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/5b262b32-5ec2-4f19-8a76-4c318aec7dc7">ImageList_BeginDrag</a> instead.]

Sets the drag image.


## -parameters




### -param him

Type: <b>HIMAGELIST</b>

A handle to an image list. This parameter uses the zero index in the ImageList.


### -param pptOffset

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A pointer to the coordinates used as the hot spot for dragging the image. The coordinates are relative to upper-left corner of the image.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.




## -remarks



You can clear the drag image by setting the <i>him</i> parameter to <code>-1</code> and the <i>pptOffset</i> parameter to <code>NULL</code>. The image must have been set within the same thread.



