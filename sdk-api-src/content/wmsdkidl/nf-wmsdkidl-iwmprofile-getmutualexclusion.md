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

# IWMProfile::GetMutualExclusion


## -description



The <b>GetMutualExclusion</b> method retrieves a mutual exclusion object from the profile.




## -parameters




### -param dwMEIndex [in]

<b>DWORD</b> containing the index of the mutual exclusion object.


### -param ppME [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a> interface of the mutual exclusion object specified by the index passed as <i>dwMEIndex</i>.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppME</i> is <b>NULL</b>, or <i>dwMEIndex</i> is outside the range of indexes available.

</td>
</tr>
</table>
 




## -remarks



You can use this method in conjunction with <a href="https://msdn.microsoft.com/c223f75b-87c6-49bd-a16a-14b4751d5f1b">GetMutualExclusionCount</a> to step through all of the mutual exclusion objects in the profile.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/efd751cf-d34d-4e74-9a00-444ec31ebef0">IWMProfile::AddMutualExclusion</a>



<a href="https://msdn.microsoft.com/eb453285-a4e5-48dd-a4d0-72d2e09badc2">IWMProfile::RemoveMutualExclusion</a>



<a href="https://msdn.microsoft.com/3a3f6763-a241-4bbd-a6e8-62041b05622d">Mutual Exclusion</a>
 

 

