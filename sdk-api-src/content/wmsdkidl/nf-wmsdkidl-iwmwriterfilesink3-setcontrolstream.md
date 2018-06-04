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

# IWMWriterFileSink3::SetControlStream


## -description



The <b>SetControlStream</b> method enables you to specify that a stream should be used as a control stream. You can also use this method to indicate that a previously specified control stream should no longer be used as a control stream.




## -parameters




### -param wStreamNumber [in]

A <b>WORD</b> specifying the stream number to configure. Stream numbers must be in the range of 1 through 63.


### -param fShouldControlStartAndStop [in]

A BOOL specifying whether or not the stream should be used as a control stream.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The stream number specified by <i>wStreamNumber</i> is greater than the maximum.

</td>
</tr>
</table>
 




## -remarks



Control streams add accuracy to <b>Start</b> and <b>Stop</b> calls. Instead of trying to find the best starting or stopping place for the file based on times in interleaved streams, the file sink starts and stops the file at exactly the specified time in the control stream. The other streams are then synchronized with the control stream.

You can have more than one control stream, by making multiple calls to this method. The file sink will start or stop at the first encountered instance of the desired time.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>
 

 

