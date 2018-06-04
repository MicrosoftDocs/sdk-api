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

# WmfPlaceableFileHeader structure


## -description


The <b>WmfPlaceableFileHeader</b> structure defines the fields of a placeable metafile header. Placeable metafiles were created as a way of specifying how a metafile is mapped and scaled on a display device.


## -struct-fields




### -field Key

Type: <b>UINT32</b>

Identification value that indicates the presence of a placeable metafile header. This value is always 0x9AC6CDD7. 


### -field Hmf

Type: <b>INT16</b>

Handle to the metafile in memory. When written to disk, this field is not used and will always contains the value 0. 


### -field BoundingBox

Type: <b><a href="https://msdn.microsoft.com/43c3a37c-0703-4bb5-9091-c33f6a388995">PWMFRect16</a></b>

Destination rectangle, measured in twips, for displaying the metafile. 


### -field Inch

Type: <b>INT16</b>

Number of twips per inch used to represent the image.

Normally, there are 1440 twips per inch; however, this number can be changed to scale the image. 
						<ul>
<li>A value of 720 specifies that the image is twice its normal size. </li>
<li>A value of 360 specifies that the image is four times its normal size. </li>
<li>A value of 2880 specifies that the image is half its normal size. </li>
</ul>



### -field Reserved

Type: <b>UINT32</b>

Not used and is always set to 0. 


### -field Checksum

Type: <b>INT16</b>

Checksum for the previous 10 <b>WORD</b><b>s</b> in the header. This value can be used to determine whether the metafile has become corrupted. 


## -remarks



Although placeable metafiles are quite common, they are not directly supported by the Windows API. To display a placeable metafile using the Windows API, you must first strip the placeable metafile header from the file. This is typically performed by copying the metafile to a temporary file starting at file offset 22 (0x16). This is because each placeable metafile begins with a 22-byte header that is followed by a standard metafile. 




## -see-also




<a href="https://msdn.microsoft.com/43c3a37c-0703-4bb5-9091-c33f6a388995">PWMFRect16</a>
 

 

