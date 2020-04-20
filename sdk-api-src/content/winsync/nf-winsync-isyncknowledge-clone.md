---
UID: NF:winsync.ISyncKnowledge.Clone
title: ISyncKnowledge::Clone (winsync.h)
description: Creates a new instance of this object, and copies the data from this object to the new object.helpviewer_keywords: ["Clone","Clone method [Windows Sync]","Clone method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","Clone method","ISyncKnowledge.Clone","ISyncKnowledge::Clone","winsync.isyncknowledge_clone","winsync/ISyncKnowledge::Clone"]
old-location: winsync\isyncknowledge_clone.htm
tech.root: winsync
ms.assetid: 4f8dbe6f-e686-464a-98d0-b6e78bfd405a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Sync], Clone method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],Clone method, ISyncKnowledge.Clone, ISyncKnowledge::Clone, winsync.isyncknowledge_clone, winsync/ISyncKnowledge::Clone
f1_keywords:
- winsync/ISyncKnowledge.Clone
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
- ISyncKnowledge.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge::Clone


## -description


Creates a new instance of this object, and copies the data from this object to the new object.


## -parameters




### -param ppClonedKnowledge [out]

Returns the newly created knowledge object.


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
 




## -remarks



The cloned knowledge object can be used independently of the original.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>
 

 

