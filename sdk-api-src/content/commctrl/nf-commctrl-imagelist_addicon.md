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

# ImageList_AddIcon macro


## -description


Adds an icon or cursor to an image list. <b>ImageList_AddIcon</b> calls the <a href="https://msdn.microsoft.com/7fa467f3-73fb-4d01-bfce-bc0a8bc90883">ImageList_ReplaceIcon</a> function. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. If this parameter identifies a masked image list, the macro copies both the image and mask bitmaps of the icon or cursor. If this parameter identifies a nonmasked image list, the macro copies only the image bitmap. 


### -param hicon

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HICON</a></b>

A handle to the icon or cursor that contains the bitmap and mask for the new image. 


## -remarks



Because the system does not save 
				<i>hicon</i>, you can destroy it after the macro returns if the icon or cursor was created by the <a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a> function. You do not need to destroy <i>hicon</i> if it was loaded by the <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> function; the system automatically frees an icon resource when it is no longer needed. 

The <b>ImageList_AddIcon</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define  ImageList_AddIcon(himl, hicon) ImageList_ReplaceIcon(himl, -1, hicon)</code></pre>


