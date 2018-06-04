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

# IWMWriterAdvanced::GetSink


## -description



The <b>GetSink</b> method retrieves a writer sink object. Used in conjunction with <a href="https://msdn.microsoft.com/210c96bc-3659-43e6-acb2-4d9f328e81e0">IWMWriterAdvanced::GetSinkCount</a>, this method can be used to enumerate the sinks associated with a writer object.




## -parameters




### -param dwSinkNum [in]

<b>DWORD</b> containing the sink number (its index). This is a number between 0 and one less than the total number of sinks associated with the file as obtained with <b>IWMWriterAdvanced::GetSinkCount</b>.


### -param ppSink [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a> interface.


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
Either the <i>ppSink</i> parameter is <b>NULL</b>, or the <i>dwSinkNum</i> parameter is greater than the number of sinks.

</td>
</tr>
</table>
 




## -remarks



You can use <b>GetSink</b> to gain access to the file sink that is automatically created when you call <a href="https://msdn.microsoft.com/352cf497-f7d6-41e8-bdbb-c59215b617a3">IWMWriter::SetOutputFilename</a>. If you are only writing to the automatically created file sink, it will always be sink number 0.




## -see-also




<a href="https://msdn.microsoft.com/1b635cd8-6bdd-4592-bfb5-bcdcf7818e18">Enumerating Sinks</a>



<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/65763ac3-fba0-4de6-9c2e-4e241bbe5f13">IWMWriterAdvanced::AddSink</a>



<a href="https://msdn.microsoft.com/210c96bc-3659-43e6-acb2-4d9f328e81e0">IWMWriterAdvanced::GetSinkCount</a>



<a href="https://msdn.microsoft.com/e2fc7f82-981a-4f69-b99d-71514ed2c6ae">IWMWriterAdvanced::RemoveSink</a>
 

 

