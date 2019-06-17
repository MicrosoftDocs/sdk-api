---
UID: NF:winsync.ISyncKnowledge.ExcludeItem
title: ISyncKnowledge::ExcludeItem (winsync.h)
author: windows-sdk-content
description: Removes knowledge about the specified item from the knowledge.
old-location: winsync\isyncknowledge_excludeitem.htm
tech.root: winsync
ms.assetid: db3cd239-dbc2-4da7-ba3d-3adc9ad1c6f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExcludeItem, ExcludeItem method [Windows Sync], ExcludeItem method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ExcludeItem method, ISyncKnowledge.ExcludeItem, ISyncKnowledge::ExcludeItem, winsync.isyncknowledge_excludeitem, winsync/ISyncKnowledge::ExcludeItem
ms.topic: method
f1_keywords: ["winsync/ISyncKnowledge.ExcludeItem"]
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
 - ISyncKnowledge.ExcludeItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge::ExcludeItem


## -description


Removes knowledge about the specified item from the knowledge.


## -parameters




### -param pbItemId [in]

The ID of the item to remove from the knowledge.


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
 

 

