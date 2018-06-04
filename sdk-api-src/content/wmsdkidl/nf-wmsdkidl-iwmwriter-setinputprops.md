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

# IWMWriter::SetInputProps


## -description



The <b>SetInputProps</b> method specifies the media properties of an input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number.


### -param pInput [in]

Pointer to an <a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps</a> interface. See Remarks.


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
<i>dwInputNum</i> is greater than the highest index number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



Manipulating the <b>IWMInputMediaProps</b> object has no effect on the writer until the application calls this method to configure the input.

Specify <b>NULL</b> for <i>pInput</i> if the input contains compressed samples that will be written directly to the new stream (using <a href="https://msdn.microsoft.com/498bfb73-bfa5-429d-ae8a-3a691fc25fc2">IWMWriterAdvanced::WriteStreamSample</a>) without being recompressed.




## -see-also




<a href="https://msdn.microsoft.com/44c4ed7e-b35e-4ab5-9975-021f343dab6a">Assigning Input Formats</a>



<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/0cb3cd79-0640-4a3b-8e8b-d81df2ff749f">IWMWriter::GetInputCount</a>



<a href="https://msdn.microsoft.com/2889a1a7-3111-4c13-b15a-659f519c22f6">IWMWriter::GetInputProps</a>
 

 

