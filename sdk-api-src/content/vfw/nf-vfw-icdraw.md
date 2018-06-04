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

# ICDraw function


## -description



The <b>ICDraw</b> function decompresses an image for drawing.




## -parameters




### -param hic

Handle to an decompressor.


### -param dwFlags

Decompression flags. The following values are defined.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Meaning
                </th>
</tr>
<tr>
<td><b>ICDRAW_HURRYUP</b></td>
<td>Data is buffered and not drawn to the screen. Use this flag for fastest decompression.</td>
</tr>
<tr>
<td><b>ICDRAW_NOTKEYFRAME</b></td>
<td>Current frame is not a key frame.</td>
</tr>
<tr>
<td><b>ICDRAW_NULLFRAME</b></td>
<td>Current frame does not contain any data and the previous frame should be redrawn.</td>
</tr>
<tr>
<td><b>ICDRAW_PREROLL</b></td>
<td>Current frame of video occurs before playback should start. For example, if playback will begin on frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 are sent to the driver with the <b>ICDRAW_PREROLL</b> flag set. The driver needs this data to display frame 10 properly.</td>
</tr>
<tr>
<td><b>ICDRAW_UPDATE</b></td>
<td>Updates the screen based on previously received data. Set <i>lpData</i> to <b>NULL</b> when this flag is used.</td>
</tr>
</table>
 


### -param lpFormat


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input format of the data.
          


### -param lpData


            Pointer to the input data.
          


### -param cbData


            Size of the input data, in bytes.
          


### -param lTime


            Time, in samples, to draw this frame. The units for video data are frames. For a definition of the playback rate, see the <b>dwRate</b> and <b>dwScale</b> members of the <a href="https://msdn.microsoft.com/1ec2309c-7ea8-423e-aee3-5e0c650f0b3d">ICDRAWBEGIN</a> structure.
          


## -returns




            Returns<b> ICERR_OK</b> if successful or an error otherwise.
          




## -remarks



You can initiate drawing the frames by sending the <a href="https://msdn.microsoft.com/d49e0d97-5a29-46f7-82d7-e3d4b4f7666f">ICM_DRAW_START</a> message (or by using the <a href="https://msdn.microsoft.com/00db96a3-d7e4-42eb-929a-c967ac8380d1">ICDrawStart</a> macro). The application should be sure to buffer the required number of frames before drawing is started. Send the <b>KM_GETBUFFERSWANTED</b> message (or use the <a href="https://msdn.microsoft.com/ed294649-d7e7-4e5f-89d4-49ed65c71b96">ICGetBuffersWanted</a> macro) to obtain this value.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

