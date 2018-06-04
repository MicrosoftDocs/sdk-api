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

# IWMWriterAdvanced::GetSinkCount


## -description



The <b>GetSinkCount</b> method retrieves the number of writer sinks associated with the writer object. To obtain a pointer to an interface of an individual sink, call <a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">IWMWriterAdvanced::GetSink</a> using a sink number between 0 and one less than the count returned by this method.




## -parameters




### -param pcSinks [out]

DWORD indicating the total number of sinks associated with the writer object.


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
<i>pcSinks</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If you specify a file by calling <a href="https://msdn.microsoft.com/352cf497-f7d6-41e8-bdbb-c59215b617a3">IWMWriter::SetOutputFilename</a>, the writer object will automatically create a file sink and add it to the writer. That sink will be included in the count retrieved by this method.




## -see-also




<a href="https://msdn.microsoft.com/1b635cd8-6bdd-4592-bfb5-bcdcf7818e18">Enumerating Sinks</a>



<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">IWMWriterAdvanced::GetSink</a>
 

 

