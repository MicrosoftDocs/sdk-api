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

# MsiRecordReadStream function


## -description


The 
<b>MsiRecordReadStream</b> function reads bytes from a record stream field into a buffer.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record.


### -param szDataBuf [out]

A buffer to receive the stream field. You should ensure the destination buffer is the same size or larger than the source buffer. See the Remarks section.


### -param pcbDataBuf [in, out]

Specifies the in and out buffer count. On input, this is the full size of the buffer. On output, this is the number of bytes that were actually written to the buffer. See the Remarks section.


## -returns



This function returns UINT.




## -remarks



To read a stream, set <i>pcbDataBuf</i> to the number of bytes that are to be transferred from stream to buffer each time the function is called. On return, the 
<b>MsiRecordReadStream</b> resets <i>pcbDataBuf </i>to the number of bytes that were actually transferred. If the buffer is smaller than the stream, the stream is repositioned when the buffer becomes full such that the next data in the stream is transferred by the next call to the function. When no more bytes are available, 
<b>MsiRecordReadStream</b> returns ERROR_SUCCESS.

If you pass 0 for <i>szDataBuf</i> then <i>pcbDataBuf</i> is reset to the number of bytes in the stream remaining to be read.

The following code sample reads from a stream that is in field 1 of a record specified by hRecord and reads the entire stream 8 bytes at a time.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>char szBuffer[8];
PMSIHANDLE hRecord;
DWORD cbBuf = sizeof(szBuffer);
do 
{
    if (MsiRecordReadStream(hRecord, 1, szBuffer, 
        &amp;cbBuf) != ERROR_SUCCESS)
        break; /* error */
}
while (cbBuf == 8);  //continue reading the stream while you receive a full buffer
//cbBuf will be less once you reach the end of the stream and cannot fill your 
//buffer with stream data
</pre>
</td>
</tr>
</table></span></div>
See also 
<a href="https://msdn.microsoft.com/ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef">OLE Limitations on Streams</a>.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

