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

# IMediaObject::ProcessInput


## -description



The <code>ProcessInput</code> method delivers a buffer to the specified input stream.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pBuffer

Pointer to the buffer's <a href="https://msdn.microsoft.com/74d72ca6-f899-43fc-bdea-5208d920f314">IMediaBuffer</a> interface.


### -param dwFlags

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/b0217926-ac2d-48e5-a5d0-e31be6ea20ac">DMO_INPUT_DATA_BUFFER_FLAGS</a> enumeration.


### -param rtTimestamp

Time stamp that specifies the start time of the data in the buffer. If the buffer has a valid time stamp, set the DMO_INPUT_DATA_BUFFERF_TIME flag in the <i>dwFlags</i> parameter. Otherwise, the DMO ignores this value.


### -param rtTimelength

Reference time specifying the duration of the data in the buffer. If this value is valid, set the DMO_INPUT_DATA_BUFFERF_TIMELENGTH flag in the <i>dwFlags</i> parameter. Otherwise, the DMO ignores this value.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
Data cannot be accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No output to process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The input buffer specified in the <i>pBuffer</i> parameter is read-only. The DMO will not modify the data in this buffer. All write operations occur on the output buffers, which are given in a separate call to the <a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a> method.

If the DMO does not process all the data in the buffer, it keeps a reference count on the buffer. It releases the buffer once it has generated all the output, unless it needs to perform lookahead on the data. (To determine whether a DMO performs lookahead, call the <a href="https://msdn.microsoft.com/9e18bf5e-cf29-4446-a1ba-422b41e02edc">IMediaObject::GetInputStreamInfo</a> method.)

If this method returns DMO_E_NOTACCEPTING, call <b>ProcessOutput</b> until the input stream can accept more data. To determine whether the stream can accept more data, call the <a href="https://msdn.microsoft.com/4581307f-cea2-4e88-81a1-972e1998c7a8">IMediaObject::GetInputStatus</a> method.

If the method returns S_FALSE, no output was generated from this input and the application does not need to call <b>ProcessOutput</b>. However, a DMO is not required to return S_FALSE in this situation; it might return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

