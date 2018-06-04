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

# IWMWriterNetworkSink::GetHostURL


## -description



The <b>GetHostURL</b> method retrieves the URL from which the stream is broadcast. Clients will access the stream from this URL.




## -parameters




### -param pwszURL [out]

Pointer to buffer that receives a string containing the URL. To retrieve the length of the string, set this parameter to <b>NULL</b>.


### -param pcchURL [in, out]

On input, pointer to the size of <i>pwszURL</i>, in characters. On output, this parameter receives the length of the URL in characters, including the terminating <b>null</b> character.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, the values shown in the following table.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>pcchURL</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is not connected.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetHostURL</b>. On the first call, pass <b>NULL</b> as <i>pwszURL</i>. On return, the value pointed to by <i>pcchURL</i> is set to the number of characters, including the terminating <b>null</b> character, required to hold the URL. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszURL</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink Interface</a>
 

 

