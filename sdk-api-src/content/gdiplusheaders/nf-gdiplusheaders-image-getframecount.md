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

# Image::GetFrameCount


## -description


The <b>Image::GetFrameCount</b> method gets the number of frames in a specified dimension of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


## -parameters




### -param dimensionID [in]

Type: <b>const GUID*</b>

Pointer to a 
					GUID that specifies the dimension. 
					GUIDs that identify various dimensions are defined in Gdiplusimaging.h. 


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the number of frames in the specified dimension of this 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.




## -see-also




<a href="https://msdn.microsoft.com/dfed0b61-2230-4911-a642-0a6e4beb08d6">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/9b61e01d-0a98-4ac3-865e-7570ed0c3cde">Creating and Saving a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/0d16501c-eedd-4cd4-85f3-f6c150b01af9">Image::GetFrameDimensionsCount</a>



<a href="https://msdn.microsoft.com/8199230e-85e9-4974-809a-32dc408d9b87">Image::GetFrameDimensionsList</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>
 

 

