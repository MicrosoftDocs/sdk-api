---
UID: NF:vfw.ICDraw
title: ICDraw function
author: windows-sdk-content
description: The ICDraw function decompresses an image for drawing.
old-location: multimedia\icdraw.htm
tech.root: Multimedia
ms.assetid: 0bf2c264-6adf-4773-95df-9cd77e73c022
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ICDraw, ICDraw function [Windows Multimedia], _win32_ICDraw, multimedia.icdraw, vfw/ICDraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<th>Value
                </th>
<th>Meaning
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
 

 

