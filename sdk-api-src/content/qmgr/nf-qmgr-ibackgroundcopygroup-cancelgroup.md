---
UID: NF:qmgr.IBackgroundCopyGroup.CancelGroup
title: IBackgroundCopyGroup::CancelGroup
author: windows-driver-content
description: Use the CancelGroup method to remove the group from the queue. Files completely downloaded before calling this method are available to the client. You can cancel a group at anytime; however, the group cannot be recovered once it is canceled.
old-location: bits\ibackgroundcopygroup_cancelgroup.htm
old-project: Bits
ms.assetid: 4ef86db1-3dff-4345-a09a-efea8b6c8c8e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CancelGroup, CancelGroup method [BITS], CancelGroup method [BITS],IBackgroundCopyGroup interface, IBackgroundCopyGroup interface [BITS],CancelGroup method, IBackgroundCopyGroup.CancelGroup, IBackgroundCopyGroup::CancelGroup, bits.ibackgroundcopygroup_cancelgroup, qmgr/IBackgroundCopyGroup::CancelGroup
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
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyGroup.CancelGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBackgroundCopyGroup::CancelGroup


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>CancelGroup</b> method to remove the group from the  queue. Files completely downloaded before calling this  method are available to the client. You can cancel a group at anytime; however, the group cannot be recovered once it is canceled.


## -parameters






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
The group was successfully canceled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

