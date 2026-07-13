---
UID: NF:qmgr.IEnumBackgroundCopyGroups.Next
title: IEnumBackgroundCopyGroups::Next (qmgr.h)
description: Use the Next method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements. (IEnumBackgroundCopyGroups.Next)
helpviewer_keywords: ["IEnumBackgroundCopyGroups interface [BITS]","Next method","IEnumBackgroundCopyGroups.Next","IEnumBackgroundCopyGroups::Next","Next","Next method [BITS]","Next method [BITS]","IEnumBackgroundCopyGroups interface","bits.ienumbackgroundcopygroups_next","qmgr/IEnumBackgroundCopyGroups::Next"]
old-location: bits\ienumbackgroundcopygroups_next.htm
tech.root: Bits
ms.assetid: cc21f663-e8f8-4348-920c-bffad46d0aa0
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyGroups interface [BITS],Next method, IEnumBackgroundCopyGroups.Next, IEnumBackgroundCopyGroups::Next, Next, Next method [BITS], Next method [BITS],IEnumBackgroundCopyGroups interface, bits.ienumbackgroundcopygroups_next, qmgr/IEnumBackgroundCopyGroups::Next
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
 - IEnumBackgroundCopyGroups::Next
 - qmgr/IEnumBackgroundCopyGroups::Next
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
 - IEnumBackgroundCopyGroups.Next
---

# IEnumBackgroundCopyGroups::Next


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>Next</b> method to retrieve the specified number of items in the enumeration sequence. If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Array of GUIDs that identify the groups. To retrieve a group, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyqmgr-getgroup">IBackgroundCopyQMgr::GetGroup</a> method with the GUID.

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

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a>
