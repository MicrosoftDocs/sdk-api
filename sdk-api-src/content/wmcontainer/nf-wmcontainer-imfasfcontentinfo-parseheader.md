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

# IMFASFContentInfo::ParseHeader


## -description



Parses the information in an ASF header and uses that information to set values in the ContentInfo object. You can pass the entire header in a single buffer or send it in several pieces.




## -parameters




### -param pIHeaderBuffer [in]

Pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of a buffer object containing some or all of the header. The buffer must contain at least 30 bytes, which is the size of the Header Object, not including the objects contained in the Header Object (that is, everything up to and including the Reserved2 field in the Header Object).


### -param cbOffsetWithinHeader [in]

Offset, in bytes, of the first byte in the buffer relative to the beginning of the header.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The header is completely parsed and validated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer does not contain valid ASF data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is to small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_ASF_PARSEINPROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but the header passed was incomplete. This is the successful return code for all calls but the last one when passing the header in pieces.

</td>
</tr>
</table>
 




## -remarks



If you pass the header in pieces, the ContentInfo object will keep references to the buffer objects until the entire header is parsed. Therefore, do not write over the buffers passed into this method.

The start of the Header object has the following layout in memory:

<table>
<tr>
<th>Field Name</th>
<th>Size in bytes</th>
</tr>
<tr>
<td>Object ID</td>
<td>16</td>
</tr>
<tr>
<td>Object Size</td>
<td>8</td>
</tr>
<tr>
<td>Number of Header Objects</td>
<td>4</td>
</tr>
<tr>
<td>Reserved1</td>
<td>1</td>
</tr>
<tr>
<td>Reserved2</td>
<td>1</td>
</tr>
</table>
 

The first call to <b>ParseHeader</b> reads everything up to and including Rerserved2, so it requires a minimum of 30 bytes. (Note that the <a href="https://msdn.microsoft.com/c13ee7e6-df59-448f-80c4-04ac7c8c98ed">IMFASFContentInfo::GetHeaderSize</a> method reads only the Object ID and Object Size fields, so that method requires a minimum of 24 bytes.)




## -see-also




<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a">Initializing the ContentInfo Object of a New ASF File</a>
 

 

