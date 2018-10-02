---
UID: NF:qmgr.IBackgroundCopyGroup.get_GroupID
title: IBackgroundCopyGroup::get_GroupID
author: windows-sdk-content
description: Use the get_GroupID method to retrieve the group's identifier.
old-location: bits\ibackgroundcopygroup_get_groupid.htm
tech.root: Bits
ms.assetid: fde4dfb9-002b-436e-96c1-a893a95dcacc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],get_GroupID method, IBackgroundCopyGroup.get_GroupID, IBackgroundCopyGroup::get_GroupID, bits.ibackgroundcopygroup_get_groupid, get_GroupID, get_GroupID method [BITS], get_GroupID method [BITS],IBackgroundCopyGroup interface, qmgr/IBackgroundCopyGroup::get_GroupID
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.get_GroupID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyGroup::get_GroupID


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>get_GroupID</b> method to retrieve the group's identifier.


## -parameters




### -param pguidGroupID

TBD




#### - pguidGroupId [out]

GUID that uniquely identifies the group within the download queue.


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
Successfully retrieved the GUID that identifies the group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

