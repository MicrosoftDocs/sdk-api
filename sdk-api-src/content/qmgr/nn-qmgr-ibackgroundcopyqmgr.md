---
UID: NN:qmgr.IBackgroundCopyQMgr
title: IBackgroundCopyQMgr (qmgr.h)
author: windows-sdk-content
description: Use the IBackgroundCopyQMgr interface to create a new group, retrieve an existing group, or enumerate all groups in the queue. A group contains a download job.
old-location: bits\ibackgroundcopyqmgr.htm
tech.root: Bits
ms.assetid: 040662c3-0d96-416a-b5e6-a16a6d3034fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyQMgr, IBackgroundCopyQMgr interface [BITS], IBackgroundCopyQMgr interface [BITS],described, bits.ibackgroundcopyqmgr, qmgr/IBackgroundCopyQMgr
ms.topic: interface
f1_keywords: 
 - "qmgr/IBackgroundCopyQMgr"
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
 - IBackgroundCopyQMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyQMgr interface


## -description


<p class="CCE_Message">[<b>IBackgroundCopyQMgr</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IBackgroundCopyQMgr</b> interface to create a new group, retrieve an existing group, or enumerate all groups in the queue. A group contains a download job.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyQMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyQMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyQMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyqmgr-creategroup">CreateGroup</a>
</td>
<td align="left" width="63%">
Creates a new group and adds it to the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyqmgr-enumgroups">EnumGroups</a>
</td>
<td align="left" width="63%">
Enumerates the groups in the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyqmgr-getgroup">GetGroup</a>
</td>
<td align="left" width="63%">
Retrieves an existing group from the queue.

</td>
</tr>
</table> 

