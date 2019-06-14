---
UID: NF:winsync.ISyncKnowledge.FindMinTickCountForReplica
title: ISyncKnowledge::FindMinTickCountForReplica (winsync.h)
author: windows-sdk-content
description: Finds the minimum tick count in the knowledge for the specified replica.
old-location: winsync\isyncknowledge_findmintickcountforreplica.htm
tech.root: winsync
ms.assetid: 6a1a3fb2-b656-4ecf-8fed-dc5f20cd22f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindMinTickCountForReplica, FindMinTickCountForReplica method [Windows Sync], FindMinTickCountForReplica method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],FindMinTickCountForReplica method, ISyncKnowledge.FindMinTickCountForReplica, ISyncKnowledge::FindMinTickCountForReplica, winsync.isyncknowledge_findmintickcountforreplica, winsync/ISyncKnowledge::FindMinTickCountForReplica
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge.FindMinTickCountForReplica
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge::FindMinTickCountForReplica


## -description


Finds the minimum tick count in the knowledge for the specified replica.


## -parameters




### -param pbReplicaId [in]

The ID of the replica to look up.


### -param pullReplicaTickCount [out]

Returns the minimum tick count in the knowledge for <i>pbReplicaId</i>.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>
 

 

