---
UID: NF:winsync.ISyncKnowledge.ProjectOntoRange
title: ISyncKnowledge::ProjectOntoRange (winsync.h)
description: Gets the knowledge for the specified range of item IDs.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","ProjectOntoRange method","ISyncKnowledge.ProjectOntoRange","ISyncKnowledge::ProjectOntoRange","ProjectOntoRange","ProjectOntoRange method [Windows Sync]","ProjectOntoRange method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_projectontorange","winsync/ISyncKnowledge::ProjectOntoRange"]
old-location: winsync\isyncknowledge_projectontorange.htm
tech.root: winsync
ms.assetid: fd82e694-088b-4695-9c5d-c9ed2a25c208
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],ProjectOntoRange method, ISyncKnowledge.ProjectOntoRange, ISyncKnowledge::ProjectOntoRange, ProjectOntoRange, ProjectOntoRange method [Windows Sync], ProjectOntoRange method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_projectontorange, winsync/ISyncKnowledge::ProjectOntoRange
f1_keywords:
- winsync/ISyncKnowledge.ProjectOntoRange
dev_langs:
- c++
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
- ISyncKnowledge.ProjectOntoRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge::ProjectOntoRange


## -description


Gets the knowledge for the specified range of item IDs.


## -parameters




### -param psrngSyncRange [in]

 The range of item IDs to look up.


### -param ppKnowledgeOut [out]

Returns a knowledge object that contains only the range of item IDs specified by <i>psrngSyncRange</i>.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsync/ns-winsync-sync_range">SYNC_RANGE Structure</a>
 

 

