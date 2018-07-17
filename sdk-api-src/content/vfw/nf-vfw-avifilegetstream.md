---
UID: NF:vfw.AVIFileGetStream
title: AVIFileGetStream function
author: windows-sdk-content
description: The AVIFileGetStream function returns the address of a stream interface that is associated with a specified AVI file.
old-location: multimedia\avifilegetstream.htm
old-project: Multimedia
ms.assetid: b51a823c-6904-4942-883f-bda347541757
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AVIFileGetStream, AVIFileGetStream function [Windows Multimedia], _win32_AVIFileGetStream, multimedia.avifilegetstream, vfw/AVIFileGetStream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIFileGetStream
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIFileGetStream function


## -description



The <b>AVIFileGetStream</b> function returns the address of a stream interface that is associated with a specified AVI file.




## -parameters




### -param pfile

Handle to an open AVI file.


### -param ppavi

Pointer to the new stream interface.


### -param fccType

Four-character code indicating the type of stream to open. Zero indicates any stream can be opened. The following definitions apply to the data commonly found in AVI streams.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>streamtypeAUDIO</td>
<td>Indicates an audio stream.</td>
</tr>
<tr>
<td>streamtypeMIDI</td>
<td>Indicates a MIDI stream.</td>
</tr>
<tr>
<td>streamtypeTEXT</td>
<td>Indicates a text stream.</td>
</tr>
<tr>
<td>streamtypeVIDEO</td>
<td>Indicates a video stream.</td>
</tr>
</table>
 


### -param lParam

Count of the stream type. Identifies which occurrence of the specified stream type to access.


## -returns



Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_NODATA</b></dt>
</dl>
</td>
<td width="60%">
The file does not contain a stream corresponding to the values of <i>fccType</i> and <i>lParam</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory.

</td>
</tr>
</table>
 




## -remarks



The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface. The argument <i>ppavi</i> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

