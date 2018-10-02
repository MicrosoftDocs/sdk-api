---
UID: NS:vfw.ICINFO
title: ICINFO
author: windows-sdk-content
description: The ICINFO structure contains compression parameters supplied by a video compression driver. The driver fills or updates the structure when it receives the ICM_GETINFO message.
old-location: multimedia\icinfo_struct.htm
tech.root: Multimedia
ms.assetid: 5faf7022-6dc8-475c-8f5a-721bc5b6afee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICINFO, ICINFO structure [Windows Multimedia], VIDCF_COMPRESSFRAMES, VIDCF_CRUNCH, VIDCF_DRAW, VIDCF_FASTTEMPORALC, VIDCF_FASTTEMPORALD, VIDCF_QUALITY, VIDCF_TEMPORAL, multimedia.icinfo_COLLISION204, multimedia.icinfo_struct, vfw/ICINFO
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
 - ICINFO
product: Windows
targetos: Windows
req.typenames: ICINFO
req.redist: 
---

# ICINFO structure


## -description



The <b>ICINFO</b> structure contains compression parameters supplied by a video compression driver. The driver fills or updates the structure when it receives the <a href="https://msdn.microsoft.com/8029f247-9777-4a34-9e84-908482094493">ICM_GETINFO</a> message.




## -struct-fields




### -field dwSize

Size, in bytes, of the <b>ICINFO</b> structure.


### -field fccType

Four-character code indicating the type of stream being compressed or decompressed. Specify "VIDC" for video streams.


### -field fccHandler

A four-character code identifying a specific compressor.


### -field dwFlags

Applicable flags. Zero or more of the following flags can be set:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="VIDCF_COMPRESSFRAMES"></a><a id="vidcf_compressframes"></a><dl>
<dt><b>VIDCF_COMPRESSFRAMES</b></dt>
</dl>
</td>
<td width="60%">
Driver is requesting to compress all frames. For information about compressing all frames, see the <a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a> message.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_CRUNCH"></a><a id="vidcf_crunch"></a><dl>
<dt><b>VIDCF_CRUNCH</b></dt>
</dl>
</td>
<td width="60%">
Driver supports compressing to a frame size.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_DRAW"></a><a id="vidcf_draw"></a><dl>
<dt><b>VIDCF_DRAW</b></dt>
</dl>
</td>
<td width="60%">
Driver supports drawing.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_FASTTEMPORALC"></a><a id="vidcf_fasttemporalc"></a><dl>
<dt><b>VIDCF_FASTTEMPORALC</b></dt>
</dl>
</td>
<td width="60%">
Driver can perform temporal compression and maintains its own copy of the current frame. When compressing a stream of frame data, the driver doesn't need image data from the previous frame.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_FASTTEMPORALD"></a><a id="vidcf_fasttemporald"></a><dl>
<dt><b>VIDCF_FASTTEMPORALD</b></dt>
</dl>
</td>
<td width="60%">
Driver can perform temporal decompression and maintains its own copy of the current frame. When decompressing a stream of frame data, the driver doesn't need image data from the previous frame.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_QUALITY"></a><a id="vidcf_quality"></a><dl>
<dt><b>VIDCF_QUALITY</b></dt>
</dl>
</td>
<td width="60%">
Driver supports quality values.

</td>
</tr>
<tr>
<td width="40%"><a id="VIDCF_TEMPORAL"></a><a id="vidcf_temporal"></a><dl>
<dt><b>VIDCF_TEMPORAL</b></dt>
</dl>
</td>
<td width="60%">
Driver supports inter-frame compression.

</td>
</tr>
</table>
 


### -field dwVersion

Version number of the driver.


### -field dwVersionICM

Version of VCM supported by the driver. This member should be set to ICVERSION.


### -field szName

Short version of the compressor name. The name in the null-terminated string should be suitable for use in list boxes.


### -field szDescription

Long version of the compressor name.


### -field szDriver

Name of the module containing VCM compression driver. Normally, a driver does not need to fill this out.


## -see-also




<a href="https://msdn.microsoft.com/d2f6f3b7-dff6-4fef-a642-cb77b00119af">ICM_COMPRESS_FRAMES_INFO</a>



<a href="https://msdn.microsoft.com/8029f247-9777-4a34-9e84-908482094493">ICM_GETINFO</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

