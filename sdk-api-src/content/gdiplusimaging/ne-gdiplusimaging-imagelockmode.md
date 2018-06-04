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

# ImageLockMode enumeration


## -description


The <b>ImageLockMode</b> enumeration specifies flags that are passed to the 
			<i>flags</i> parameter of the 
			<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a> method. The <b>Bitmap::LockBits</b> method locks a portion of an image so that you can read or write the pixel data.


## -enum-fields




### -field ImageLockModeRead

Specifies that a portion of the image is locked for reading. 


### -field ImageLockModeWrite

Specifies that a portion of the image is locked for writing. 


### -field ImageLockModeUserInputBuf

Specifies that the buffer used for reading or writing pixel data is allocated by the user. If this flag is set, then the 
				<i>lockedBitmapData</i> parameter of the 
				<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a> method serves as an input parameter (and possibly as an output parameter). If this flag is cleared, then the 
				<i>lockedBitmapData</i> parameter serves only as an output parameter. 


## -see-also




<a href="https://msdn.microsoft.com/f67a53d1-62bb-4e68-aef2-c3282de1ef40">Bitmap::LockBits</a>
 

 

