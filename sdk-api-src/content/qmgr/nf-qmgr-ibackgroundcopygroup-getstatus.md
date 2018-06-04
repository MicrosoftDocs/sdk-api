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

# IBackgroundCopyGroup::GetStatus


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>GetStatus</b> method to retrieve the state of the group.


## -parameters




### -param pdwStatus [out]

State of the group. The state can be set to one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_GROUP_FOREGROUND"></a><a id="qm_status_group_foreground"></a><dl>
<dt><b>QM_STATUS_GROUP_FOREGROUND</b></dt>
</dl>
</td>
<td width="60%">
QMGR is downloading the group in the foreground.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_GROUP_INCOMPLETE"></a><a id="qm_status_group_incomplete"></a><dl>
<dt><b>QM_STATUS_GROUP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
QMGR is still downloading the group.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_GROUP_SUSPENDED"></a><a id="qm_status_group_suspended"></a><dl>
<dt><b>QM_STATUS_GROUP_SUSPENDED</b></dt>
</dl>
</td>
<td width="60%">
The group is suspended.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_GROUP_ERROR"></a><a id="qm_status_group_error"></a><dl>
<dt><b>QM_STATUS_GROUP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while processing the group. 

</td>
</tr>
</table>
 


### -param pdwJobIndex

Current job in progress. The index is always 0 (groups can only contain one job).


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
Successfully retrieved the state of the group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

