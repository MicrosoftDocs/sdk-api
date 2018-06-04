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

# Shell_GetImageLists function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Retrieves system image lists for large and small icons.


## -parameters




### -param phiml [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for large (32 x 32) icons.


### -param phimlSmall [in]

Type: <b>HIMAGELIST*</b>

A pointer to the handle of an image list which, on success, receives the system image list for small (16 x 16) icons.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> on success. On failure, returns <b>FALSE</b> and the image lists pointed to by <i>phiml</i> and <i>phimlSmall</i> are unchanged.




## -remarks



<div class="alert"><b>Important</b>  The image lists retrieved through this function are global system image lists; do not call <a href="https://msdn.microsoft.com/6720c9e7-b35f-4acd-8fa7-9aa9f0991879">ImageList_Destroy</a> using them.</div>
<div> </div>



## -see-also




<a href="_win32_Image_Lists">Image Lists</a>



<a href="https://msdn.microsoft.com/d662bedf-4be0-4528-8121-e7923a42bc67">SHGetFileInfo</a>



<a href="https://msdn.microsoft.com/6ae80c1f-f2b7-4da9-b588-30391c8aef0e">SHGetImageList</a>
 

 

