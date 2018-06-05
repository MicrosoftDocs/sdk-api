---
UID: NF:qmgr.IBackgroundCopyGroup.GetStatus
title: IBackgroundCopyGroup::GetStatus
author: windows-sdk-content
description: Use the GetStatus method to retrieve the state of the group.
old-location: bits\ibackgroundcopygroup_getstatus.htm
old-project: Bits
ms.assetid: 9ac76e50-a2cf-4dfb-af7e-803ee483f0f9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetStatus, GetStatus method [BITS], GetStatus method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],GetStatus method, IBackgroundCopyGroup.GetStatus, IBackgroundCopyGroup::GetStatus, QM_STATUS_GROUP_ERROR, QM_STATUS_GROUP_FOREGROUND, QM_STATUS_GROUP_INCOMPLETE, QM_STATUS_GROUP_SUSPENDED, bits.ibackgroundcopygroup_getstatus, qmgr/IBackgroundCopyGroup::GetStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyGroup.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

