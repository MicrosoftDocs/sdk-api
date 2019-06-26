---
UID: NN:qmgr.IBackgroundCopyGroup
title: IBackgroundCopyGroup (qmgr.h)
author: windows-sdk-content
description: Use the IBackgroundCopyGroup interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.
old-location: bits\ibackgroundcopygroup.htm
tech.root: Bits
ms.assetid: 51ddd89a-489a-4b83-ad45-838809a6d2e8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup, IBackgroundCopyGroup interface [BITS], IBackgroundCopyGroup interface [BITS],described, bits.ibackgroundcopygroup, qmgr/IBackgroundCopyGroup
ms.topic: interface
f1_keywords: 
 - "qmgr/IBackgroundCopyGroup"
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
 - IBackgroundCopyGroup
 - IBackgroundCopyGroup.InternalSetProp
 - IBackgroundCopyGroup.QueryNewJobInterface
 - IBackgroundCopyGroup.SetNotificationPointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyGroup interface


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IBackgroundCopyGroup</b> interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyGroup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-cancelgroup">CancelGroup</a>
</td>
<td align="left" width="63%">
Cancels all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-createjob">CreateJob</a>
</td>
<td align="left" width="63%">
Creates a new job and adds it to the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-enumjobs">EnumJobs</a>
</td>
<td align="left" width="63%">
Retrieves a list of jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-get_groupid">get_GroupID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier that uniquely identifies the group within the download queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-get_size">get_Size</a>
</td>
<td align="left" width="63%">
Retrieves the calculated size of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-getjob">GetJob</a>
</td>
<td align="left" width="63%">
Retrieves a job from the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-getprop">GetProp</a>
</td>
<td align="left" width="63%">
Retrieves a group property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the state of the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>InternalSetProp</b></td>
<td align="left" width="63%">
Internal use only. Use <a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-setprop">SetProp</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>QueryNewJobInterface</b></td>
<td align="left" width="63%">
Internal use only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-resumegroup">ResumeGroup</a>
</td>
<td align="left" width="63%">
Resumes the download of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetNotificationPointer</b></td>
<td align="left" width="63%">
Internal use only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-setprop">SetProp</a>
</td>
<td align="left" width="63%">
Sets a group property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-suspendgroup">SuspendGroup</a>
</td>
<td align="left" width="63%">
Suspends the download of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-switchtoforeground">SwitchToForeground</a>
</td>
<td align="left" width="63%">
Downloads the group in the foreground instead of the background.

</td>
</tr>
</table> 

