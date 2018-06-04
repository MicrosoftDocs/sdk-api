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

# IBackgroundCopyQMgr::GetGroup


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/040662c3-0d96-416a-b5e6-a16a6d3034fc">IBackgroundCopyQMgr</a> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetGroup</b> method to retrieve a group from the download queue. The current user can retrieve only groups that they own. If the user has Administrator privileges, the user can retrieve any group from the download queue. Retrieving a group from the queue transfers ownership of the group to the current user.


## -parameters




### -param groupID




### -param ppGroup [out]

Pointer to an <a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a> interface pointer. Use this interface to manage the group. For example, add a job to the group and set the properties of the group. 


#### - guidGroupId [in]

GUID that uniquely identifies the group in the download queue.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the group. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>QM_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find the group in the download queue.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/040662c3-0d96-416a-b5e6-a16a6d3034fc">IBackgroundCopyQMgr</a>
 

 

