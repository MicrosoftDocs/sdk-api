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

# IWMWriterAdvanced::GetWriterTime


## -description



The <b>GetWriterTime</b> method retrieves the clock time that the writer is working to.




## -parameters




### -param pcnsCurrentTime [out]

Pointer to a variable containing the current time in 100-nanosecond units.


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
<i>pcnsCurrentTime</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method returns the largest time stamp that the writer can currently process. This time stamp will increase as data is produced by the writer. This method can be used to ensure that data is delivered to the writer at the proper rate.

The time returned is the number of 100-nanosecond units since the call to <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>.

The writer can be running in real time. Call the <a href="https://msdn.microsoft.com/3d00eb78-d90e-41a0-9bba-305ac65057f3">IWMWriterAdvanced::IsRealTime</a> method to ascertain whether this is true.




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>
 

 

