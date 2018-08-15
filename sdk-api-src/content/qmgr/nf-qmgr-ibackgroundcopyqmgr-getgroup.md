---
UID: NF:qmgr.IBackgroundCopyQMgr.GetGroup
title: IBackgroundCopyQMgr::GetGroup
author: windows-sdk-content
description: Use the GetGroup method to retrieve a group from the download queue.
old-location: bits\ibackgroundcopyqmgr_getgroup.htm
old-project: bits
ms.assetid: 36836fe5-4858-4c6e-8ce8-1bb71c8e9f5a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetGroup, GetGroup method [BITS], GetGroup method [BITS],IBackgroundCopyQMgr interface, IBackgroundCopyQMgr interface [BITS],GetGroup method, IBackgroundCopyQMgr.GetGroup, IBackgroundCopyQMgr::GetGroup, bits.ibackgroundcopyqmgr_getgroup, qmgr/IBackgroundCopyQMgr::GetGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyQMgr.GetGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: ADAM
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
 

 

