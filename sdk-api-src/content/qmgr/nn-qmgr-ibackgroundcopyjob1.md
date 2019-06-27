---
UID: NN:qmgr.IBackgroundCopyJob1
title: IBackgroundCopyJob1 (qmgr.h)
author: windows-sdk-content
description: Use the IBackgroundCopyJob1 interface to add files to the job and retrieve the job's status.
old-location: bits\ibackgroundcopyjob1.htm
tech.root: Bits
ms.assetid: ccf1b355-c1af-4b5e-b613-181c426ed777
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob1, IBackgroundCopyJob1 interface [BITS], IBackgroundCopyJob1 interface [BITS],described, bits.ibackgroundcopyjob1, qmgr/IBackgroundCopyJob1
ms.topic: interface
f1_keywords: 
 - "qmgr/IBackgroundCopyJob1"
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
 - IBackgroundCopyJob1
 - IBackgroundCopyJob1.CancelJob
 - IBackgroundCopyJob1.SwitchToForeground
 - IBackgroundCopyJob1.GetTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyJob1 interface


## -description


<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IBackgroundCopyJob1</b> interface to add files to the job and retrieve the job's status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob1</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyJob1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-addfiles">AddFiles</a>
</td>
<td align="left" width="63%">
Adds one or more files to the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CancelJob</b></td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getfile">GetFile</a>
</td>
<td align="left" width="63%">
Retrieves the remote and local names of a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getfilecount">GetFileCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of files to download in the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the download progress of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the state of the job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>GetTimes</b></td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SwitchToForeground</b></td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

