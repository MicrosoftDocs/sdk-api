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

# ICCOMPRESS structure


## -description



The <b>ICCOMPRESS</b> structure contains compression parameters used with the <a href="https://msdn.microsoft.com/d95b943f-458d-4a5e-bab1-e3648d323395">ICM_COMPRESS</a> message.




## -struct-fields




### -field dwFlags

Flags used for compression. The following value is defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICCOMPRESS_KEYFRAME"></a><a id="iccompress_keyframe"></a><dl>
<dt><b>ICCOMPRESS_KEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Input data should be treated as a key frame.

</td>
</tr>
</table>
 


### -field lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output (compressed) format. The <b>biSizeImage</b> member must contain the size of the compressed data.


### -field lpOutput


            Pointer to the buffer where the driver should write the compressed data.
          


### -field lpbiInput


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input (uncompressed) format.
          


### -field lpInput


            Pointer to the buffer containing input data.
          


### -field lpckid


            Address to contain the chunk identifier for data in the AVI file. If the value of this member is not <b>NULL</b>, the driver should specify a two-character code for the chunk identifier corresponding to the chunk identifier used in the AVI file.
          


### -field lpdwFlags


            Address to contain flags for the AVI index. If the returned frame is a key frame, the driver should set the <b>AVIIF_KEYFRAME</b> flag.
          


### -field lFrameNum


            Number of the frame to compress.
          


### -field dwFrameSize


            Desired maximum size, in bytes, for compressing this frame. The size value is used for compression methods that can make tradeoffs between compressed image size and image quality. Specify zero for this member to use the default setting.
          


### -field dwQuality


            Quality setting.
          


### -field lpbiPrev


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the format of the previous frame, which is typically the same as the input format.
          


### -field lpPrev


            Pointer to the buffer containing input data of the previous frame.
          


## -remarks



Drivers that perform temporal compression use data from the previous frame (found in the <b>lpbiPrev</b> and <b>lpPrev</b> members) to prune redundant data from the current frame.




## -see-also




<a href="https://msdn.microsoft.com/d95b943f-458d-4a5e-bab1-e3648d323395">ICM_COMPRESS</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

