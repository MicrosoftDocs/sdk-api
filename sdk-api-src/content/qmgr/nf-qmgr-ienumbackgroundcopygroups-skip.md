---
UID: NF:qmgr.IEnumBackgroundCopyGroups.Skip
title: IEnumBackgroundCopyGroups::Skip (qmgr.h)
description: Use the Skip method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence. (IEnumBackgroundCopyGroups.Skip)
helpviewer_keywords: ["IEnumBackgroundCopyGroups interface [BITS]","Skip method","IEnumBackgroundCopyGroups.Skip","IEnumBackgroundCopyGroups::Skip","Skip","Skip method [BITS]","Skip method [BITS]","IEnumBackgroundCopyGroups interface","bits.ienumbackgroundcopygroups_skip","qmgr/IEnumBackgroundCopyGroups::Skip"]
old-location: bits\ienumbackgroundcopygroups_skip.htm
tech.root: Bits
ms.assetid: 27e907d0-1b2a-44d2-b401-0b28d5a8b340
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyGroups interface [BITS],Skip method, IEnumBackgroundCopyGroups.Skip, IEnumBackgroundCopyGroups::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBackgroundCopyGroups interface, bits.ienumbackgroundcopygroups_skip, qmgr/IEnumBackgroundCopyGroups::Skip
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
 - IEnumBackgroundCopyGroups::Skip
 - qmgr/IEnumBackgroundCopyGroups::Skip
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
 - IEnumBackgroundCopyGroups.Skip
---

# IEnumBackgroundCopyGroups::Skip


## -description

<p class="CCE_Message">[<b>IEnumBackgroundCopyGroups</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>Skip</b> method to skip the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

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
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ienumbackgroundcopygroups">IEnumBackgroundCopyGroups</a>
