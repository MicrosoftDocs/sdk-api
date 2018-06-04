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

# IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto


## -description


Converts an image resource from a JpegXR to an HD Photo.


## -parameters




### -param imageResource

[in, out] The image resource to convert. 

When the method returns, the converted image resource.


## -returns



Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded. 

XPS_E_INVALID_CONTENT_TYPE: The image type is not XPS_IMAGE_TYPE_JXR.

E_INVALIDARG if data is not recognized by WDP decoder or another error occurred.




## -remarks



This image referenced by imageResource is changed from an XPS_IMAGE_TYPE_JPEGXR image type to an XPS_IMAGE_TYPE_WDP image type. This method converts the data stream of the image resource;, however, the part name of the resource remains the same.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

