---
UID: NF:winsync.ISyncKnowledge.Union
title: ISyncKnowledge::Union (winsync.h)
description: Combines the specified knowledge with the current knowledge.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","Union method","ISyncKnowledge.Union","ISyncKnowledge::Union","Union","Union method [Windows Sync]","Union method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_union","winsync/ISyncKnowledge::Union"]
old-location: winsync\isyncknowledge_union.htm
tech.root: winsync
ms.assetid: 95d88d28-57b7-4b4a-abda-a69f25b1e8b8
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],Union method, ISyncKnowledge.Union, ISyncKnowledge::Union, Union, Union method [Windows Sync], Union method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_union, winsync/ISyncKnowledge::Union
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
 - ISyncKnowledge::Union
 - winsync/ISyncKnowledge::Union
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
 - ISyncKnowledge.Union
---

# ISyncKnowledge::Union


## -description

Combines the specified knowledge with the current knowledge.

## -parameters

### -param pKnowledge [in]

The knowledge to combine with the current knowledge.

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
The method succeeded.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>