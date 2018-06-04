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
 

 

