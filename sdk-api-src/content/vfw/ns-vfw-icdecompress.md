---
UID: NS:vfw.ICDECOMPRESS
title: ICDECOMPRESS
author: windows-sdk-content
description: The ICDECOMPRESS structure contains decompression parameters used with the ICM_DECOMPRESS message.
old-location: multimedia\icdecompress_struct.htm
old-project: Multimedia
ms.assetid: bc9c2416-cc1c-4571-82ee-7d93307f5114
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ICDECOMPRESS, ICDECOMPRESS structure [Windows Multimedia], ICDECOMPRESS_HURRYUP, ICDECOMPRESS_NOTKEYFRAME, ICDECOMPRESS_NULLFRAME, ICDECOMPRESS_PREROLL, ICDECOMPRESS_UPDATE, multimedia.icdecompress_COLLISION813, multimedia.icdecompress_struct, vfw/ICDECOMPRESS
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: ICDECOMPRESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICDECOMPRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDECOMPRESS structure


## -description



The <b>ICDECOMPRESS</b> structure contains decompression parameters used with the <a href="https://msdn.microsoft.com/666f2ebf-80a5-4846-861d-c79c3001c5a0">ICM_DECOMPRESS</a> message.




## -struct-fields




### -field dwFlags

Applicable flags. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_HURRYUP"></a><a id="icdecompress_hurryup"></a><dl>
<dt><b>ICDECOMPRESS_HURRYUP</b></dt>
</dl>
</td>
<td width="60%">

                Tries to decompress at a faster rate. When an application uses this flag, the driver should buffer the decompressed data but not draw the image.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_NOTKEYFRAME"></a><a id="icdecompress_notkeyframe"></a><dl>
<dt><b>ICDECOMPRESS_NOTKEYFRAME</b></dt>
</dl>
</td>
<td width="60%">

                Current frame is not a key frame.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_NULLFRAME"></a><a id="icdecompress_nullframe"></a><dl>
<dt><b>ICDECOMPRESS_NULLFRAME</b></dt>
</dl>
</td>
<td width="60%">

                Current frame does not contain data and the decompressed image should be left the same.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_PREROLL"></a><a id="icdecompress_preroll"></a><dl>
<dt><b>ICDECOMPRESS_PREROLL</b></dt>
</dl>
</td>
<td width="60%">

                Current frame precedes the point in the movie where playback starts and, therefore, will not be drawn.
              

</td>
</tr>
<tr>
<td width="40%"><a id="ICDECOMPRESS_UPDATE"></a><a id="icdecompress_update"></a><dl>
<dt><b>ICDECOMPRESS_UPDATE</b></dt>
</dl>
</td>
<td width="60%">

                Screen is being updated or refreshed.
              

</td>
</tr>
</table>
 


### -field lpbiInput


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input format.
          


### -field lpInput


            Pointer to a buffer containing the input data.
          


### -field lpbiOutput


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format.
          


### -field lpOutput


            Pointer to a buffer where the driver should write the decompressed image.
          


### -field ckid


            Chunk identifier from the AVI file.
          


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=16915">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/666f2ebf-80a5-4846-861d-c79c3001c5a0">ICM_DECOMPRESS</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

