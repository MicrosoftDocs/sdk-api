---
UID: NN:qmgr.IBackgroundCopyGroup
title: IBackgroundCopyGroup
author: windows-sdk-content
description: Use the IBackgroundCopyGroup interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.
old-location: bits\ibackgroundcopygroup.htm
tech.root: bits
ms.assetid: 51ddd89a-489a-4b83-ad45-838809a6d2e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyGroup, IBackgroundCopyGroup interface [BITS], IBackgroundCopyGroup interface [BITS],described, bits.ibackgroundcopygroup, qmgr/IBackgroundCopyGroup
ms.topic: interface
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
---

# IBackgroundCopyGroup interface


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>IBackgroundCopyGroup</b> interface to manage a group. A group contains download jobs. For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBackgroundCopyGroup</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4ef86db1-3dff-4345-a09a-efea8b6c8c8e">CancelGroup</a>
</td>
<td align="left" width="63%">
Cancels all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2453996e-f994-43b9-901b-680a55095268">CreateJob</a>
</td>
<td align="left" width="63%">
Creates a new job and adds it to the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40e4412e-60d5-4e08-85b9-1e92f5222e71">EnumJobs</a>
</td>
<td align="left" width="63%">
Retrieves a list of jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fde4dfb9-002b-436e-96c1-a893a95dcacc">get_GroupID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier that uniquely identifies the group within the download queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69190b6a-6920-4f84-9109-12079f00a6ae">get_Size</a>
</td>
<td align="left" width="63%">
Retrieves the calculated size of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c392e9e2-0489-457b-b21a-dfff9e2c0f39">GetJob</a>
</td>
<td align="left" width="63%">
Retrieves a job from the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a596a005-a3ad-4d2b-b19b-60c2279590da">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c27debdf-22eb-417e-b870-2891167f4498">GetProp</a>
</td>
<td align="left" width="63%">
Retrieves a group property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ac76e50-a2cf-4dfb-af7e-803ee483f0f9">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the state of the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>InternalSetProp</b></td>
<td align="left" width="63%">
Internal use only. Use <a href="https://msdn.microsoft.com/057a1004-fbe6-4c90-84c0-4e5b55539ce9">SetProp</a>.

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
<a href="https://msdn.microsoft.com/a9b0b7df-9149-4d09-a37c-c0a4f5dc6e45">ResumeGroup</a>
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
<a href="https://msdn.microsoft.com/057a1004-fbe6-4c90-84c0-4e5b55539ce9">SetProp</a>
</td>
<td align="left" width="63%">
Sets a group property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac7600dd-3943-46cf-ad2d-f33d0099f2af">SuspendGroup</a>
</td>
<td align="left" width="63%">
Suspends the download of all jobs in the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19619a97-b4f2-4609-9b06-bb188e00860c">SwitchToForeground</a>
</td>
<td align="left" width="63%">
Downloads the group in the foreground instead of the background.

</td>
</tr>
</table> 

