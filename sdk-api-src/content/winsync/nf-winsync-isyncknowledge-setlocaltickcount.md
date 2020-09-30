---
UID: NF:winsync.ISyncKnowledge.SetLocalTickCount
title: ISyncKnowledge::SetLocalTickCount (winsync.h)
description: Sets the tick count for the replica that owns this knowledge.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","SetLocalTickCount method","ISyncKnowledge.SetLocalTickCount","ISyncKnowledge::SetLocalTickCount","SetLocalTickCount","SetLocalTickCount method [Windows Sync]","SetLocalTickCount method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_setlocaltickcount","winsync/ISyncKnowledge::SetLocalTickCount"]
old-location: winsync\isyncknowledge_setlocaltickcount.htm
tech.root: winsync
ms.assetid: 0da3728d-c2b8-4998-bdc4-50642af9e416
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],SetLocalTickCount method, ISyncKnowledge.SetLocalTickCount, ISyncKnowledge::SetLocalTickCount, SetLocalTickCount, SetLocalTickCount method [Windows Sync], SetLocalTickCount method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_setlocaltickcount, winsync/ISyncKnowledge::SetLocalTickCount
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
 - ISyncKnowledge::SetLocalTickCount
 - winsync/ISyncKnowledge::SetLocalTickCount
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
 - ISyncKnowledge.SetLocalTickCount
---

# ISyncKnowledge::SetLocalTickCount


## -description

Sets the tick count for the replica that owns this knowledge.

## -parameters

### -param ullTickCount [in]

The current tick count for the replica that owns this knowledge.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

The tick count must be current before the knowledge is sent to another replica. Typically, a provider calls this method immediately before it sends its knowledge; however, the method can be called at any time.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>