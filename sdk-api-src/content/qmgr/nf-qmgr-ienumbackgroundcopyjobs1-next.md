---
UID: NF:qmgr.IEnumBackgroundCopyJobs1.Next
title: IEnumBackgroundCopyJobs1::Next (qmgr.h)
description: Use the Next method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements. (IEnumBackgroundCopyJobs1.Next)
helpviewer_keywords: ["IEnumBackgroundCopyJobs1 interface [BITS]","Next method","IEnumBackgroundCopyJobs1.Next","IEnumBackgroundCopyJobs1::Next","Next","Next method [BITS]","Next method [BITS]","IEnumBackgroundCopyJobs1 interface","bits.ienumbackgroundcopyjobs1_next","qmgr/IEnumBackgroundCopyJobs1::Next"]
old-location: bits\ienumbackgroundcopyjobs1_next.htm
tech.root: Bits
ms.assetid: 15dcc2e1-7fdf-4c4a-a24b-2cad49bda7fc
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyJobs1 interface [BITS],Next method, IEnumBackgroundCopyJobs1.Next, IEnumBackgroundCopyJobs1::Next, Next, Next method [BITS], Next method [BITS],IEnumBackgroundCopyJobs1 interface, bits.ienumbackgroundcopyjobs1_next, qmgr/IEnumBackgroundCopyJobs1::Next
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
 - IEnumBackgroundCopyJobs1::Next
 - qmgr/IEnumBackgroundCopyJobs1::Next
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
 - IEnumBackgroundCopyJobs1.Next
---

# IEnumBackgroundCopyJobs1::Next


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyJobs1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>Next</b> method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of GUIDs that identify the jobs. To retrieve a job, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-getjob">IBackgroundCopyGroup::GetJob</a> method with the GUID.

### -param pceltFetched [out]

Number of elements in <i>rgelt</i>. You can set <i>pceltFetched</i> to <b>NULL</b> if <i>celt</i> is one.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned less than the number of requested elements.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopyjobs1">IEnumBackgroundCopyJobs1</a>
