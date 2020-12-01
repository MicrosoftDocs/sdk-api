---
UID: NF:winsync.ISyncKnowledge.GetReplicaKeyMap
title: ISyncKnowledge::GetReplicaKeyMap (winsync.h)
description: Gets the IReplicaKeyMap object that is associated with this knowledge.
helpviewer_keywords: ["GetReplicaKeyMap","GetReplicaKeyMap method [Windows Sync]","GetReplicaKeyMap method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","GetReplicaKeyMap method","ISyncKnowledge.GetReplicaKeyMap","ISyncKnowledge::GetReplicaKeyMap","winsync.isyncknowledge_getreplicakeymap","winsync/ISyncKnowledge::GetReplicaKeyMap"]
old-location: winsync\isyncknowledge_getreplicakeymap.htm
tech.root: winsync
ms.assetid: 5f4052f8-ad58-4805-be75-5456d2d1e7bc
ms.date: 12/05/2018
ms.keywords: GetReplicaKeyMap, GetReplicaKeyMap method [Windows Sync], GetReplicaKeyMap method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetReplicaKeyMap method, ISyncKnowledge.GetReplicaKeyMap, ISyncKnowledge::GetReplicaKeyMap, winsync.isyncknowledge_getreplicakeymap, winsync/ISyncKnowledge::GetReplicaKeyMap
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
 - ISyncKnowledge::GetReplicaKeyMap
 - winsync/ISyncKnowledge::GetReplicaKeyMap
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
 - ISyncKnowledge.GetReplicaKeyMap
---

# ISyncKnowledge::GetReplicaKeyMap


## -description

Gets the <b>IReplicaKeyMap</b> object that is associated with this knowledge.

## -parameters

### -param ppReplicaKeyMap [out]

Returns the <b>IReplicaKeyMap</b> object that is associated with this knowledge.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ireplicakeymap">IReplicaKeyMap Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>