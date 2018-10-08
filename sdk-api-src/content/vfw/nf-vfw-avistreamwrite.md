---
UID: NF:vfw.AVIStreamWrite
title: AVIStreamWrite function
author: windows-sdk-content
description: The AVIStreamWrite function writes data to a stream.
old-location: multimedia\avistreamwrite.htm
tech.root: Multimedia
ms.assetid: 9a306939-7b4f-4e0b-8340-270725da74c3
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: AVIIF_KEYFRAME, AVIStreamWrite, AVIStreamWrite function [Windows Multimedia], _win32_AVIStreamWrite, multimedia.avistreamwrite, vfw/AVIStreamWrite
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
req.dll: Avifil32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVIStreamWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamWrite function


## -description



The <b>AVIStreamWrite</b> function writes data to a stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param lStart

First sample to write.


### -param lSamples

Number of samples to write.


### -param lpBuffer

Pointer to a buffer containing the data to write.


### -param cbBuffer

Size of the buffer referenced by <i>lpBuffer</i>.


### -param dwFlags

Flag associated with this data. The following flag is defined:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVIIF_KEYFRAME"></a><a id="aviif_keyframe"></a><dl>
<dt><b>AVIIF_KEYFRAME</b></dt>
</dl>
</td>
<td width="60%">
Indicates this data does not rely on preceding data in the file.

</td>
</tr>
</table>
 


### -param plSampWritten

Pointer to a buffer that receives the number of samples written. This can be set to <b>NULL</b>.


### -param plBytesWritten

Pointer to a buffer that receives the number of bytes written. This can be set to <b>NULL</b>.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The default AVI file handler supports writing only at the end of a stream. The "WAVE" file handler supports writing anywhere.

This function overwrites existing data, rather than inserting new data.

The argument <i>pavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

