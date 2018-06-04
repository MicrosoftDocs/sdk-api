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

# IWMStreamPrioritization::GetPriorityRecords


## -description



The <b>GetPriorityRecords</b> method retrieves the list of streams and their priorities from the profile.




## -parameters




### -param pRecordArray [out]

Pointer to an array of <b>WM_STREAM_PRIORITY_RECORD</b> structures. This array will receive the current stream priority data.


### -param pcRecords [in, out]

Pointer to a <b>WORD</b> that receives the count of records.


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
<i>pcRecords</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
<i>pcRecords</i> specifies fewer records than exist in the stream prioritization object.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetPriorityRecords</b>. On the first call, pass <b>NULL</b> as <i>pRecordArray</i>. On return, the value of <i>pcRecords</i> is set to the number of prioritization records in the stream priority object. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pRecordArray</i> in the second call.

If you pass an array as <i>pRecordArray</i> that does not have enough elements allocated to contain the data, an error code of ASF_E_BUFFERTOOSMALL is returned. When returning this error code, the method still sets the value of <i>pcRecords</i>.

Records in a stream prioritization object are given in order of decreasing priority




## -see-also




<a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/9bd42132-b391-4941-87db-5ce2254e19cf">IWMStreamPrioritization::SetPriorityRecords</a>



<a href="https://msdn.microsoft.com/43c9370c-cd43-4dd0-8258-d6dbdb98f1de">WM_STREAM_PRIORITY_RECORD</a>
 

 

