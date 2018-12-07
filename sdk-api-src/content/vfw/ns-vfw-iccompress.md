---
UID: NS:vfw.ICCOMPRESS
title: ICCOMPRESS
author: windows-sdk-content
description: The ICCOMPRESS structure contains compression parameters used with the ICM_COMPRESS message.
old-location: multimedia\iccompress_struct.htm
tech.root: Multimedia
ms.assetid: ba6aec9c-b622-484b-88ce-ff5c659bd6d7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICCOMPRESS, ICCOMPRESS structure [Windows Multimedia], ICCOMPRESS_KEYFRAME, multimedia.iccompress_COLLISION455, multimedia.iccompress_struct, vfw/ICCOMPRESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICCOMPRESS
product: Windows
targetos: Windows
req.typenames: ICCOMPRESS
req.redist: 
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
 

 

