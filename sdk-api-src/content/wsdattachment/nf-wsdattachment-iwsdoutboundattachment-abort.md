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

# IWSDOutboundAttachment::Abort


## -description


Aborts the transfer of data on the attachment MIME data stream. When <b>Abort</b> is called, any pending data may be discarded.


## -parameters






## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/add0160c-bbf7-446e-8592-a05fd4d16fac">Abort</a> was called before <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> was called. You must call <b>Write</b> before terminating the attachment stream.

</td>
</tr>
</table>
 




## -remarks



The <b>Abort</b> method may be called when a <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a> method call failed with the error <b>STG_S_BLOCK</b>.


<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> must not be called once <b>Abort</b> has been called on an attachment stream.




## -see-also




<a href="https://msdn.microsoft.com/ba2f2038-e6ef-4ad4-a1fb-50e225394c60">IWSDOutboundAttachment</a>



<a href="https://msdn.microsoft.com/8ab63ed5-7b71-4f28-926d-a24666f0dd15">IWSDOutboundAttachment::Close</a>



<a href="https://msdn.microsoft.com/5bd24e7c-f2f4-4cc4-abc0-176ed024fa43">IWSDOutboundAttachment::Write</a>
 

 

