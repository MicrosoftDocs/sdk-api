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

# IWMStreamList::GetStreams


## -description



The <b>GetStreams</b> method retrieves an array of stream numbers that make up the list.




## -parameters




### -param pwStreamNumArray [out]

Pointer to a <b>WORD</b> array containing the stream numbers. Pass <b>NULL</b> to retrieve the required size of the array.


### -param pcStreams [in, out]

On input, a pointer to a variable containing the size of the <i>pwStreamNumArray</i> array. On output, if the method succeeds, this variable contains the number of stream numbers entered into <i>pwStreamNumArray</i> by the method.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcStreams</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The input value of <i>pcStreams</i> is not large enough.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetStreams</b>. On the first call, pass <b>NULL</b> as <i>pwStreamNumArray</i>. On return, the value pointed to by <i>pcStreams</i> is set to the number of stream numbers in the stream number array. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pwStreamNumArray</i> on the second call.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList Interface</a>
 

 

