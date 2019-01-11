---
UID: NF:qmgr.IBackgroundCopyGroup.ResumeGroup
title: IBackgroundCopyGroup::ResumeGroup
author: windows-sdk-content
description: Use the ResumeGroup method to start a group that has been suspended in the download queue.
old-location: bits\ibackgroundcopygroup_resumegroup.htm
tech.root: Bits
ms.assetid: a9b0b7df-9149-4d09-a37c-c0a4f5dc6e45
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],ResumeGroup method, IBackgroundCopyGroup.ResumeGroup, IBackgroundCopyGroup::ResumeGroup, ResumeGroup, ResumeGroup method [BITS], ResumeGroup method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_resumegroup, qmgr/IBackgroundCopyGroup::ResumeGroup
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
 - IBackgroundCopyGroup.ResumeGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyGroup::ResumeGroup


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>ResumeGroup</b> method to start a group that has been suspended in the download queue.


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
Successfully resumed the group in the download queue.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

