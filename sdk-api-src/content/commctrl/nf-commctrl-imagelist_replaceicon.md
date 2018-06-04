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

# ImageList_ReplaceIcon function


## -description


Replaces an image with an icon or cursor.


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i [in]

Type: <b>int</b>

The index of the image to replace. If 
					<i>i</i> is -1, the function appends the image to the end of the list. 


### -param hicon [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a></b>

The handle to the icon or cursor that contains the bitmap and mask for the new image. 


## -returns



Type: <b>int</b>

Returns the index of the image if successful, or -1 otherwise.




## -remarks



Because the system does not save 
				<i>hicon</i>, you can destroy it after the function returns if the icon or cursor was created by the <a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a> function. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 



