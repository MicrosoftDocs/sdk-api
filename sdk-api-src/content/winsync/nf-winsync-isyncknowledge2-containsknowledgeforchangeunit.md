---
UID: NF:winsync.ISyncKnowledge2.ContainsKnowledgeForChangeUnit
title: ISyncKnowledge2::ContainsKnowledgeForChangeUnit (winsync.h)
description: Indicates whether the specified knowledge of the specified change unit is known by this knowledge.
helpviewer_keywords: ["ContainsKnowledgeForChangeUnit","ContainsKnowledgeForChangeUnit method [Windows Sync]","ContainsKnowledgeForChangeUnit method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","ContainsKnowledgeForChangeUnit method","ISyncKnowledge2.ContainsKnowledgeForChangeUnit","ISyncKnowledge2::ContainsKnowledgeForChangeUnit","winsync.isyncknowledge2_containsknowledgeforchangeunit","winsync/ISyncKnowledge2::ContainsKnowledgeForChangeUnit"]
old-location: winsync\isyncknowledge2_containsknowledgeforchangeunit.htm
tech.root: winsync
ms.assetid: ecaefb24-eca0-408c-a98d-f7e6bbfefade
ms.date: 12/05/2018
ms.keywords: ContainsKnowledgeForChangeUnit, ContainsKnowledgeForChangeUnit method [Windows Sync], ContainsKnowledgeForChangeUnit method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],ContainsKnowledgeForChangeUnit method, ISyncKnowledge2.ContainsKnowledgeForChangeUnit, ISyncKnowledge2::ContainsKnowledgeForChangeUnit, winsync.isyncknowledge2_containsknowledgeforchangeunit, winsync/ISyncKnowledge2::ContainsKnowledgeForChangeUnit
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
 - ISyncKnowledge2::ContainsKnowledgeForChangeUnit
 - winsync/ISyncKnowledge2::ContainsKnowledgeForChangeUnit
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
 - ISyncKnowledge2.ContainsKnowledgeForChangeUnit
---

# ISyncKnowledge2::ContainsKnowledgeForChangeUnit


## -description

Indicates whether the specified knowledge of the specified change unit is known by this knowledge.

## -parameters

### -param pKnowledge [in]

The knowledge object that contains knowledge about <i>pbChangeUnitId</i>.

### -param pbItemId [in]

The ID of the item that contains the change unit to look up.

### -param pbChangeUnitId [in]

The ID of the change unit to look up.

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
This object contains the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain the knowledge known by <i>pKnowledge</i> about <i>pbChangeUnitId</i>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER
</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is not of the format specified by the provider.

</td>
</tr>
</table>

## -remarks

Another way to obtain the same result is to pass <i>pbItemId</i> and <i>pbChangeUnitId</i> to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containschangeunit">ISyncKnowledge::ContainsChangeUnit</a> method of <i>pKnowledge</i>, and then take the resulting projected knowledge and pass it to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containsknowledge">ISyncKnowledge::ContainsKnowledge</a> method of this object.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>