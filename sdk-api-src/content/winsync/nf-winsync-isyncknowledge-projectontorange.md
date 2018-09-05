---
UID: NF:winsync.ISyncKnowledge.ProjectOntoRange
title: ISyncKnowledge::ProjectOntoRange
author: windows-sdk-content
description: Gets the knowledge for the specified range of item IDs.
old-location: winsync\isyncknowledge_projectontorange.htm
old-project: winsync
ms.assetid: fd82e694-088b-4695-9c5d-c9ed2a25c208
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],ProjectOntoRange method, ISyncKnowledge.ProjectOntoRange, ISyncKnowledge::ProjectOntoRange, ProjectOntoRange, ProjectOntoRange method [Windows Sync], ProjectOntoRange method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_projectontorange, winsync/ISyncKnowledge::ProjectOntoRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge.ProjectOntoRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/d3e4a4f4-4a67-4dce-a81a-3861dcf788e6">SYNC_RANGE Structure</a>
 

 

