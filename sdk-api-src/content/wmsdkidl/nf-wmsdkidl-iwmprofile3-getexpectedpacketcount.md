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

# IWMProfile3::GetExpectedPacketCount


## -description



The <b>GetExpectedPacketCount</b> method calculates the expected <a href="wmformat_glossary.htm">packet</a> count for the specified duration. The packet count returned is only an estimate, and it is based upon the settings of the profile at the time this call is made.




## -parameters




### -param msDuration [in]

Specifies the duration in milliseconds.


### -param pcPackets [out]

Pointer to receive the count of packets expected for <i>msDuration</i> milliseconds.


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
<i>pcPackets</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
One of the internal objects required by the method could not be initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The profile in the profile object is not compatible with this method.

</td>
</tr>
</table>
 




## -remarks



Problems will arise if the value passed in <i>msDuration</i> is not a positive number of milliseconds. The method will return S_OK as normal, but the packet count returned will not be correct.

It is impossible for this method to give exact counts, because there is no way to account for interleaved data in an encoded file. The packet count returned is most accurate for files with one audio stream. The more complicated the profile, the less accurate the packet count will be.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>
 

 

