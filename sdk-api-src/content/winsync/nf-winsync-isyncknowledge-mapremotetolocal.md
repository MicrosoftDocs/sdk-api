---
UID: NF:winsync.ISyncKnowledge.MapRemoteToLocal
title: ISyncKnowledge::MapRemoteToLocal (winsync.h)
description: Converts a knowledge object from another replica into one that is compatible with the replica that owns this knowledge.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","MapRemoteToLocal method","ISyncKnowledge.MapRemoteToLocal","ISyncKnowledge::MapRemoteToLocal","MapRemoteToLocal","MapRemoteToLocal method [Windows Sync]","MapRemoteToLocal method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_mapremotetolocal","winsync/ISyncKnowledge::MapRemoteToLocal"]
old-location: winsync\isyncknowledge_mapremotetolocal.htm
tech.root: winsync
ms.assetid: 9325ff3e-4f8e-4a18-bc95-57af30ccd437
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],MapRemoteToLocal method, ISyncKnowledge.MapRemoteToLocal, ISyncKnowledge::MapRemoteToLocal, MapRemoteToLocal, MapRemoteToLocal method [Windows Sync], MapRemoteToLocal method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_mapremotetolocal, winsync/ISyncKnowledge::MapRemoteToLocal
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
 - ISyncKnowledge::MapRemoteToLocal
 - winsync/ISyncKnowledge::MapRemoteToLocal
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
 - ISyncKnowledge.MapRemoteToLocal
---

# ISyncKnowledge::MapRemoteToLocal


## -description

Converts a knowledge object from another replica into one that is compatible with the replica that owns this knowledge.

## -parameters

### -param pRemoteKnowledge [in]

A knowledge object that is owned by another replica.

### -param ppMappedKnowledge [out]

Returns the knowledge object, converted for use by the replica that owns this knowledge.

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