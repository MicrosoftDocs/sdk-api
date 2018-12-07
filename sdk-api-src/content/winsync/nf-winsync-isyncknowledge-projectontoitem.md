---
UID: NF:winsync.ISyncKnowledge.ProjectOntoItem
title: ISyncKnowledge::ProjectOntoItem
author: windows-sdk-content
description: Gets the knowledge for the specified item.
old-location: winsync\isyncknowledge_projectontoitem.htm
tech.root: winsync
ms.assetid: 069fdc90-bea3-42e4-835c-b2a397d13b60
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],ProjectOntoItem method, ISyncKnowledge.ProjectOntoItem, ISyncKnowledge::ProjectOntoItem, ProjectOntoItem, ProjectOntoItem method [Windows Sync], ProjectOntoItem method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_projectontoitem, winsync/ISyncKnowledge::ProjectOntoItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncKnowledge.ProjectOntoItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge::ProjectOntoItem


## -description


Gets the knowledge for the specified item.


## -parameters




### -param pbItemId [in]

The ID of the item to look up.


### -param ppKnowledgeOut [out]

Returns a knowledge object that contains only the item specified by <i>pbItemId</i>.


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
 

 

