---
UID: NF:winsync.ISyncKnowledge2.IntersectsWithKnowledge
title: ISyncKnowledge2::IntersectsWithKnowledge (winsync.h)
description: Indicates whether the specified knowledge intersects with this knowledge.
helpviewer_keywords: ["ISyncKnowledge2 interface [Windows Sync]","IntersectsWithKnowledge method","ISyncKnowledge2.IntersectsWithKnowledge","ISyncKnowledge2::IntersectsWithKnowledge","IntersectsWithKnowledge","IntersectsWithKnowledge method [Windows Sync]","IntersectsWithKnowledge method [Windows Sync]","ISyncKnowledge2 interface","winsync.isyncknowledge2_intersectswithknowledge","winsync/ISyncKnowledge2::IntersectsWithKnowledge"]
old-location: winsync\isyncknowledge2_intersectswithknowledge.htm
tech.root: winsync
ms.assetid: 8d2ce743-7827-4ee4-a800-3ba706d4a7a6
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge2 interface [Windows Sync],IntersectsWithKnowledge method, ISyncKnowledge2.IntersectsWithKnowledge, ISyncKnowledge2::IntersectsWithKnowledge, IntersectsWithKnowledge, IntersectsWithKnowledge method [Windows Sync], IntersectsWithKnowledge method [Windows Sync],ISyncKnowledge2 interface, winsync.isyncknowledge2_intersectswithknowledge, winsync/ISyncKnowledge2::IntersectsWithKnowledge
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncKnowledge2::IntersectsWithKnowledge
 - winsync/ISyncKnowledge2::IntersectsWithKnowledge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge2.IntersectsWithKnowledge
---

# ISyncKnowledge2::IntersectsWithKnowledge


## -description

Indicates whether the specified knowledge intersects with this knowledge.

## -parameters

### -param pSyncKnowledge [in]

The knowledge that is checked against this object to determine whether there is an intersection.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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
The specified knowledge intersects with this knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified knowledge does not intersect with this knowledge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>