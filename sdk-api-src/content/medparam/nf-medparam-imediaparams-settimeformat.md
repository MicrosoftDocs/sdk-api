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

# IMediaParams::SetTimeFormat


## -description



The <code>SetTimeFormat</code> method specifies the time format for the object.




## -parameters




### -param guidTimeFormat [in]

Time format GUID that specifies the time format.


### -param mpTimeData [in]

Value of type <b>MP_TIMEDATA</b> that specifies the unit of measure for the new format.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Object does not support this time format.

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



Objects can support more than one time format. Every object must support reference time, in which each unit of time is 100 nanoseconds (ns). Other formats are optional. The application must ensure that time stamps on the input buffers match whatever time format was set using this method.

The meaning of the <i>mpTimeData</i> parameter depends on the value of the <i>guidTimeFormat</i> parameter.

<table>
<tr>
<th>
              Time Format
            </th>
<th>
              Meaning of Time Data
            </th>
</tr>
<tr>
<td>GUID_TIME_MUSIC</td>
<td>Parts per quarter note.</td>
</tr>
<tr>
<td>GUID_TIME_REFERENCE</td>
<td>Ignored.</td>
</tr>
<tr>
<td>GUID_TIME_SAMPLES</td>
<td>Samples per second.</td>
</tr>
</table>
 

When you call this method, also call the <a href="https://msdn.microsoft.com/574d6573-ea5d-4419-ad65-f5f7d711e720">FlushEnvelope</a> method, to flush any envelopes that were set using the previous time format.

To determine what time formats an object supports, call the <a href="https://msdn.microsoft.com/04e4c9ea-4570-4fd0-986b-c835c692b73b">IMediaParamInfo::GetSupportedTimeFormat</a> method. To retrieve the current format, call the <a href="https://msdn.microsoft.com/b93b929c-c1a7-4e8e-93cf-118fcd6a3de9">IMediaParamInfo::GetCurrentTimeFormat</a> method.




## -see-also




<a href="https://msdn.microsoft.com/68ea8f6a-4b6d-4d79-a986-6032b767147b">IMediaParams Interface</a>



<a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>
 

 

