---
UID: NF:winsync.ISyncKnowledge.ContainsKnowledge
title: ISyncKnowledge::ContainsKnowledge (winsync.h)
description: Indicates whether the specified knowledge is known by this knowledge.
helpviewer_keywords: ["ContainsKnowledge","ContainsKnowledge method [Windows Sync]","ContainsKnowledge method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","ContainsKnowledge method","ISyncKnowledge.ContainsKnowledge","ISyncKnowledge::ContainsKnowledge","winsync.isyncknowledge_containsknowledge","winsync/ISyncKnowledge::ContainsKnowledge"]
old-location: winsync\isyncknowledge_containsknowledge.htm
tech.root: winsync
ms.assetid: b6b58390-84be-48ff-a3b9-3b3c83d4f661
ms.date: 12/05/2018
ms.keywords: ContainsKnowledge, ContainsKnowledge method [Windows Sync], ContainsKnowledge method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ContainsKnowledge method, ISyncKnowledge.ContainsKnowledge, ISyncKnowledge::ContainsKnowledge, winsync.isyncknowledge_containsknowledge, winsync/ISyncKnowledge::ContainsKnowledge
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
 - ISyncKnowledge::ContainsKnowledge
 - winsync/ISyncKnowledge::ContainsKnowledge
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
 - ISyncKnowledge.ContainsKnowledge
---

# ISyncKnowledge::ContainsKnowledge


## -description

Indicates whether the specified knowledge is known by this knowledge.

## -parameters

### -param pKnowledge [in]

The knowledge to look up.

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
<i>pSyncKnowledge</i> is known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>pSyncKnowledge</i> is not known.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>