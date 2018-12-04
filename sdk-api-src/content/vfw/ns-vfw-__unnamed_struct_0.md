---
UID: NS:vfw.__unnamed_struct_0
title: ICOPEN
author: windows-sdk-content
description: The ICOPEN structure contains information about the data stream being compressed or decompressed, the version number of the driver, and how the driver is used.
old-location: multimedia\icopen_struct.htm
tech.root: Multimedia
ms.assetid: 6c29961c-7f9c-49e5-84aa-a5f4ff1cbbd1
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ICMODE_COMPRESS, ICMODE_DECOMPRESS, ICMODE_DRAW, ICMODE_QUERY, ICOPEN, ICOPEN structure [Windows Multimedia], multimedia.icopen_COLLISION563, multimedia.icopen_struct, vfw/ICOPEN
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
 - ICOPEN
product: Windows
targetos: Windows
req.typenames: ICOPEN
req.redist: 
---

# ICOPEN structure


## -description



The <b>ICOPEN</b> structure contains information about the data stream being compressed or decompressed, the version number of the driver, and how the driver is used.




## -struct-fields




### -field dwSize

Size, in bytes, of the structure.


### -field fccType

Four-character code indicating the type of stream being compressed or decompressed. Specify "VIDC" for video streams.


### -field fccHandler

Four-character code identifying a specific compressor.


### -field dwVersion

Version of the installable driver interface used to open the driver.


### -field dwFlags

Applicable flags indicating why the driver is opened. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICMODE_COMPRESS"></a><a id="icmode_compress"></a><dl>
<dt><b>ICMODE_COMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Driver is opened to compress data.

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DECOMPRESS"></a><a id="icmode_decompress"></a><dl>
<dt><b>ICMODE_DECOMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Driver is opened to decompress data.

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DRAW"></a><a id="icmode_draw"></a><dl>
<dt><b>ICMODE_DRAW</b></dt>
</dl>
</td>
<td width="60%">
Device driver is opened to decompress data directly to hardware.

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_QUERY"></a><a id="icmode_query"></a><dl>
<dt><b>ICMODE_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Driver is opened for informational purposes, rather than for compression.

</td>
</tr>
</table>
 


### -field dwError


### -field pV1Reserved

Reserved; do not use.


### -field pV2Reserved

Reserved; do not use.


### -field dnDevNode

Device node for plug and play devices.


## -remarks



This structure is passed to video capture drivers when they are opened. This allows a single installable driver to function as either an installable compressor or a video capture device. By examining the <b>fccType</b> member of the <b>ICOPEN</b> structure, the driver can determine its function. For example, a <b>fccType</b> value of "VIDC" indicates that it is opened as an installable video compressor.




## -see-also




<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>



<a href="https://msdn.microsoft.com/129a65a7-cac3-47e0-9e9c-6e5a4a260c73">Video Compression Structures</a>
 

 

