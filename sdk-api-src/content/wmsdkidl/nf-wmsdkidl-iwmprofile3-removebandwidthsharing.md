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

# IWMProfile3::RemoveBandwidthSharing


## -description



The <b>RemoveBandwidthSharing</b> method removes a bandwidth sharing object from the profile. If you do not already have a pointer to the <a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing</a> interface of the object you want to remove, you must obtain one with a call to <a href="https://msdn.microsoft.com/be66ff8b-c883-4329-aaa4-e9549d0cbb9e">IWMProfile3::GetBandwidthSharing</a>.




## -parameters




### -param pBS [in]

Pointer to a bandwidth sharing object.


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
<i>pBS</i> is <b>NULL</b>.

OR

The bandwidth sharing object pointed to by <i>pBS</i> is not part of the profile.

</td>
</tr>
</table>
 




## -remarks



This method does not release the bandwidth sharing object from memory. You must make a call to the <b>Release</b> method.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>



<a href="https://msdn.microsoft.com/174a4583-93fb-41cd-ba14-a959a28c1ea3">IWMProfile3::AddBandwidthSharing</a>
 

 

