---
UID: NN:qmgr.IEnumBackgroundCopyJobs1
title: IEnumBackgroundCopyJobs1 (qmgr.h)
description: Use the IEnumBackgroundCopyJobs1 interface to enumerate the list of jobs in a group. To get an IEnumBackgroundCopyJobs1 interface pointer, call the IBackgroundCopyGroup::EnumJobs method.
helpviewer_keywords: ["IEnumBackgroundCopyJobs1","IEnumBackgroundCopyJobs1 interface [BITS]","IEnumBackgroundCopyJobs1 interface [BITS]","described","bits.ienumbackgroundcopyjobs1","qmgr/IEnumBackgroundCopyJobs1"]
old-location: bits\ienumbackgroundcopyjobs1.htm
tech.root: Bits
ms.assetid: 93feac90-8eb8-49d8-9841-d78a2645fbcb
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyJobs1, IEnumBackgroundCopyJobs1 interface [BITS], IEnumBackgroundCopyJobs1 interface [BITS],described, bits.ienumbackgroundcopyjobs1, qmgr/IEnumBackgroundCopyJobs1
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumBackgroundCopyJobs1
 - qmgr/IEnumBackgroundCopyJobs1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IEnumBackgroundCopyJobs1
---

# IEnumBackgroundCopyJobs1 interface


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>IEnumBackgroundCopyJobs1</b> interface to enumerate the list of jobs in a group. To get an <b>IEnumBackgroundCopyJobs1</b> interface pointer, call the <a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-enumjobs">IBackgroundCopyGroup::EnumJobs</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBackgroundCopyJobs1</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyJobs1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBackgroundCopyJobs1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ienumbackgroundcopyjobs1-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ienumbackgroundcopyjobs1-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ienumbackgroundcopyjobs1-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ienumbackgroundcopyjobs1-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/qmgr/nf-qmgr-ienumbackgroundcopyjobs1-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table>

