---
UID: NF:winsync.ISyncKnowledge2.ContainsKnowledgeForItem
title: ISyncKnowledge2::ContainsKnowledgeForItem (winsync.h)
description: Indicates whether the specified knowledge of the specified item is known by this knowledge.
helpviewer_keywords: ["ContainsKnowledgeForItem","ContainsKnowledgeForItem method [Windows Sync]","ContainsKnowledgeForItem method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","ContainsKnowledgeForItem method","ISyncKnowledge2.ContainsKnowledgeForItem","ISyncKnowledge2::ContainsKnowledgeForItem","winsync.isyncknowledge2_containsknowledgeforitem","winsync/ISyncKnowledge2::ContainsKnowledgeForItem"]
old-location: winsync\isyncknowledge2_containsknowledgeforitem.htm
tech.root: winsync
ms.assetid: 5359e50d-8541-40ed-8107-a904ac62bfe0
ms.date: 12/05/2018
ms.keywords: ContainsKnowledgeForItem, ContainsKnowledgeForItem method [Windows Sync], ContainsKnowledgeForItem method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],ContainsKnowledgeForItem method, ISyncKnowledge2.ContainsKnowledgeForItem, ISyncKnowledge2::ContainsKnowledgeForItem, winsync.isyncknowledge2_containsknowledgeforitem, winsync/ISyncKnowledge2::ContainsKnowledgeForItem
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
 - ISyncKnowledge2::ContainsKnowledgeForItem
 - winsync/ISyncKnowledge2::ContainsKnowledgeForItem
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
 - ISyncKnowledge2.ContainsKnowledgeForItem
---

# ISyncKnowledge2::ContainsKnowledgeForItem


## -description

Indicates whether the specified knowledge of the specified item is known by this knowledge.

## -parameters

### -param pKnowledge [in]

The knowledge object that contains knowledge about <i>pbItemId</i>.

### -param pbItemId [in]

The ID of the item to look up.

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
This object contains the knowledge known by <i>pKnowledge</i> about <i>pbItemId</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain the knowledge known by <i>pKnowledge</i> about <i>pbItemId</i>.

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
<i>pbItemId</i> is not of the format specified by the provider.

</td>
</tr>
</table>

## -remarks

Another way to obtain the same result is to pass <i>pbItemId</i> to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontoitem">ISyncKnowledge::ProjectOntoItem</a> method of <i>pKnowledge</i>, and then take the resulting projected knowledge and pass it to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-containsknowledge">ISyncKnowledge::ContainsKnowledge</a> method of this object.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>