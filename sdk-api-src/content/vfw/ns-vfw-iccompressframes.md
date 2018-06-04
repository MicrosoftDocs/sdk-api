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

# ICCOMPRESSFRAMES structure


## -description



The <b>ICCOMPRESSFRAMES</b> structure contains compression parameters used with the <a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a> message.




## -struct-fields




### -field dwFlags


            Applicable flags. The following value is defined: <b>ICCOMPRESSFRAMES_PADDING</b>. If this value is used, padding is used with the frame.
          


### -field lpbiOutput


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format.
          


### -field lOutput


            Reserved; do not use.
          


### -field lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input format.


### -field lInput

Reserved; do not use.


### -field lStartFrame

Number of the first frame to compress.


### -field lFrameCount

Number of frames to compress.


### -field lQuality

Quality setting.


### -field lDataRate

Maximum data rate, in bytes per second.


### -field lKeyRate

Maximum number of frames between consecutive key frames.


### -field dwRate

Compression rate in an integer format. To obtain the rate in frames per second, divide this value by the value in <b>dwScale</b>.


### -field dwScale

Value used to scale <b>dwRate</b> to frames per second.


### -field dwOverheadPerFrame

Reserved; do not use.


### -field dwReserved2

Reserved; do not use.


### -field GetData

Reserved; do not use.


### -field PutData

Reserved; do not use.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=16915">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a>



Video Compression Manager



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

