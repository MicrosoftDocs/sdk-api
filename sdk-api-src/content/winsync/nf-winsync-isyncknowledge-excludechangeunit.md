---
UID: NF:winsync.ISyncKnowledge.ExcludeChangeUnit
title: ISyncKnowledge::ExcludeChangeUnit (winsync.h)
description: Removes knowledge about the specified change unit from the knowledge.
helpviewer_keywords: ["ExcludeChangeUnit","ExcludeChangeUnit method [Windows Sync]","ExcludeChangeUnit method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","ExcludeChangeUnit method","ISyncKnowledge.ExcludeChangeUnit","ISyncKnowledge::ExcludeChangeUnit","winsync.isyncknowledge_excludechangeunit","winsync/ISyncKnowledge::ExcludeChangeUnit"]
old-location: winsync\isyncknowledge_excludechangeunit.htm
tech.root: winsync
ms.assetid: 0b9e39a8-6610-468a-a0e6-3950b8c17d58
ms.date: 12/05/2018
ms.keywords: ExcludeChangeUnit, ExcludeChangeUnit method [Windows Sync], ExcludeChangeUnit method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ExcludeChangeUnit method, ISyncKnowledge.ExcludeChangeUnit, ISyncKnowledge::ExcludeChangeUnit, winsync.isyncknowledge_excludechangeunit, winsync/ISyncKnowledge::ExcludeChangeUnit
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
 - ISyncKnowledge::ExcludeChangeUnit
 - winsync/ISyncKnowledge::ExcludeChangeUnit
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
 - ISyncKnowledge.ExcludeChangeUnit
---

# ISyncKnowledge::ExcludeChangeUnit


## -description

Removes knowledge about the specified change unit from the knowledge.

## -parameters

### -param pbItemId [in]

The ID of the item that contains the change unit to exclude from the knowledge.

### -param pbChangeUnitId [in]

The ID of the change unit to exclude from the knowledge.

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