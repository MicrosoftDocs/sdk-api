---
UID: NF:winsync.ISyncKnowledge2.ProjectOntoColumnSet
title: ISyncKnowledge2::ProjectOntoColumnSet (winsync.h)
description: Returns the knowledge for the specified set of change units for all the items that are contained in this object.
helpviewer_keywords: ["ISyncKnowledge2 interface [Windows Sync]","ProjectOntoColumnSet method","ISyncKnowledge2.ProjectOntoColumnSet","ISyncKnowledge2::ProjectOntoColumnSet","ProjectOntoColumnSet","ProjectOntoColumnSet method [Windows Sync]","ProjectOntoColumnSet method [Windows Sync]","ISyncKnowledge2 interface","winsync.isyncknowledge2_projectontocolumnset","winsync/ISyncKnowledge2::ProjectOntoColumnSet"]
old-location: winsync\isyncknowledge2_projectontocolumnset.htm
tech.root: winsync
ms.assetid: fe183377-9b5a-476b-91af-ff974a9d41a4
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge2 interface [Windows Sync],ProjectOntoColumnSet method, ISyncKnowledge2.ProjectOntoColumnSet, ISyncKnowledge2::ProjectOntoColumnSet, ProjectOntoColumnSet, ProjectOntoColumnSet method [Windows Sync], ProjectOntoColumnSet method [Windows Sync],ISyncKnowledge2 interface, winsync.isyncknowledge2_projectontocolumnset, winsync/ISyncKnowledge2::ProjectOntoColumnSet
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
 - ISyncKnowledge2::ProjectOntoColumnSet
 - winsync/ISyncKnowledge2::ProjectOntoColumnSet
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
 - ISyncKnowledge2.ProjectOntoColumnSet
---

# ISyncKnowledge2::ProjectOntoColumnSet


## -description

Returns the knowledge for the specified set of change units for all the items that are contained in this object.

## -parameters

### -param ppColumns [in]

The set of change unit IDs to look up.

### -param count [in]

The number of change unit IDs that are contained in <i>ppColumns</i>.

### -param ppiKnowledgeOut [out]

A knowledge object that contains only the change units that are specified by <i>ppColumns</i> for all items contained in this object.

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
<td width="60%">
<i>count</i> is zero.

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
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The format of the change unit IDs that is contained in <i>ppColumns</i> is not of the format that the format schema of the provider specified.

</td>
</tr>
</table>

## -remarks

<b>ProjectOntoColumnSet</b> differs from <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge-projectontochangeunit">ISyncKnowledge::ProjectOntoChangeUnit</a>. <b>ProjectOntoColumnSet</b> returns a knowledge object that contains information about the specified set of change units for all the items that are contained in the knowledge object. <b>ProjectOntoChangeUnit</b> returns a knowledge object that contains information about a single change unit that is contained in a single item.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>