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

# TBREPLACEBITMAP structure


## -description


Used with the <a href="https://msdn.microsoft.com/abad5c7a-ebdd-46b5-a465-fe64ff8eb127">TB_REPLACEBITMAP</a> message to replace one toolbar bitmap with another.


## -struct-fields




### -field hInstOld

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Module instance handle to the bitmap resource being replaced. Set this member to <b>NULL</b> to instead use a bitmap handle. 


### -field nIDOld

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

If 
					<b>hInstOld</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap that is being replaced. Otherwise, set it to the resource identifier of the bitmap being replaced. 


### -field hInstNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Module instance handle that contains the new bitmap resource. Set this member to <b>NULL</b> to instead use a bitmap handle. 


### -field nIDNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

If 
					<b>hInstNew</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap with the new button images. Otherwise, set it to the resource identifier of the bitmap with the new button images. 


### -field nButtons

Type: <b>int</b>

Number of button images contained in the new bitmap. The number of new images should be the same as the number of replaced images.


## -remarks



If 
				<b>nIDNew</b> holds a bitmap handle, rather than a resource ID, do not destroy the bitmap until it has been replaced with <a href="https://msdn.microsoft.com/abad5c7a-ebdd-46b5-a465-fe64ff8eb127">TB_REPLACEBITMAP</a>, or the toolbar is destroyed.



