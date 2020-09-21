---
UID: NF:winsync.ISyncKnowledge.ProjectOntoChangeUnit
title: ISyncKnowledge::ProjectOntoChangeUnit (winsync.h)
description: Gets the knowledge for the specified change unit.
helpviewer_keywords: ["ISyncKnowledge interface [Windows Sync]","ProjectOntoChangeUnit method","ISyncKnowledge.ProjectOntoChangeUnit","ISyncKnowledge::ProjectOntoChangeUnit","ProjectOntoChangeUnit","ProjectOntoChangeUnit method [Windows Sync]","ProjectOntoChangeUnit method [Windows Sync]","ISyncKnowledge interface","winsync.isyncknowledge_projectontochangeunit","winsync/ISyncKnowledge::ProjectOntoChangeUnit"]
old-location: winsync\isyncknowledge_projectontochangeunit.htm
tech.root: winsync
ms.assetid: 3c09284f-9866-49a4-adeb-561af3351ada
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge interface [Windows Sync],ProjectOntoChangeUnit method, ISyncKnowledge.ProjectOntoChangeUnit, ISyncKnowledge::ProjectOntoChangeUnit, ProjectOntoChangeUnit, ProjectOntoChangeUnit method [Windows Sync], ProjectOntoChangeUnit method [Windows Sync],ISyncKnowledge interface, winsync.isyncknowledge_projectontochangeunit, winsync/ISyncKnowledge::ProjectOntoChangeUnit
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
 - ISyncKnowledge::ProjectOntoChangeUnit
 - winsync/ISyncKnowledge::ProjectOntoChangeUnit
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
 - ISyncKnowledge.ProjectOntoChangeUnit
---

# ISyncKnowledge::ProjectOntoChangeUnit


## -description

Gets the knowledge for the specified change unit.

## -parameters

### -param pbItemId [in]

The ID of the item that contains the change unit to look up.

### -param pbChangeUnitId [in]

The ID of the change unit to look up.

### -param ppKnowledgeOut [out]

Returns a knowledge object that contains only the change unit specified by <i>pbChangeUnitId</i>.

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