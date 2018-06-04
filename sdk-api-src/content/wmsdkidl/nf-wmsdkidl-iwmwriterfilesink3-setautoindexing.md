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

# IWMWriterFileSink3::SetAutoIndexing


## -description



The <b>SetAutoIndexing</b> method enables or disables automatic indexing of the file.




## -parameters




### -param fDoAutoIndexing [in]

Boolean value that is True to automatically index the file.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The header has already been received

</td>
</tr>
</table>
 




## -remarks



The state of automatic indexing must be set before the header is processed. After the header has been processed, any call to <b>SetAutoIndexing</b> results in an error.

Files are indexed by default. To disable indexing, you must call this method, passing False as the parameter.

If you generate an ASF file using bit-rate mutual exclusion for audio content (multiple bit-rate audio), the resulting indexed file will not work with Windows Media Services version 4.1. If you want to stream your file using Windows Media Services 4.1, you must disable automatic indexing before writing the file.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/a6412ce4-03ac-4777-8eb2-ef9f265a6d6c">IWMWriterFileSink3::GetAutoIndexing</a>



<a href="https://msdn.microsoft.com/7daa4b29-0597-462d-ad65-135d0ef7362d">Working with Indexes</a>
 

 

