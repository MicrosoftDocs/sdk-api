---
UID: NF:vfw.AVIStreamOpenFromFileW
title: AVIStreamOpenFromFileW function
author: windows-sdk-content
description: The AVIStreamOpenFromFile function opens a single stream from a file.
old-location: multimedia\avistreamopenfromfile.htm
tech.root: Multimedia
ms.assetid: f9ac2a8a-08b7-42a7-b71b-a1d44c924b20
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AVIStreamOpenFromFile, AVIStreamOpenFromFile function [Windows Multimedia], AVIStreamOpenFromFileA, AVIStreamOpenFromFileW, _win32_AVIStreamOpenFromFile, multimedia.avistreamopenfromfile, vfw/AVIStreamOpenFromFile, vfw/AVIStreamOpenFromFileA, vfw/AVIStreamOpenFromFileW
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
req.unicode-ansi: AVIStreamOpenFromFileW (Unicode) and AVIStreamOpenFromFileA (ANSI)
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
 - AVIStreamOpenFromFile
 - AVIStreamOpenFromFileA
 - AVIStreamOpenFromFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamOpenFromFileW function


## -description



The <b>AVIStreamOpenFromFile</b> function opens a single stream from a file.




## -parameters




### -param ppavi

Pointer to a buffer that receives the new stream handle.


### -param szFile

Null-terminated string containing the name of the file to open.


### -param fccType

Four-character code indicating the type of stream to be opened. Zero indicates that any stream can be opened. The following definitions apply to the data commonly found in AVI streams:

<table>
<tr>
<th>Value
                </th>
<th>Description
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

Stream of the type specified in <i>fccType</i> to access. This parameter is zero-based; use zero to specify the first occurrence.


### -param mode

Access mode to use when opening the file. This function can open only existing streams, so the OF_CREATE mode flag cannot be used. For more information about the available flags for the <i>mode</i> parameter, see the <b>OpenFile</b> function.


### -param pclsidHandler

Pointer to a class identifier of the handler you want to use. If the value is <b>NULL</b>, the system chooses one from the registry based on the file extension or the file RIFF type.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



This function calls the <a href="https://msdn.microsoft.com/a5d7b278-7c80-42a3-94a4-5c012ad9a9fd">AVIFileOpen</a>, <a href="https://msdn.microsoft.com/b51a823c-6904-4942-883f-bda347541757">AVIFileGetStream</a>, and <a href="https://msdn.microsoft.com/c2f94ca2-b46c-48b0-9c31-92cf2cf75be3">AVIFileRelease</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

