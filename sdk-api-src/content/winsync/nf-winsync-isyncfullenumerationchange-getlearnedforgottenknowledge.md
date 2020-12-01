---
UID: NF:winsync.ISyncFullEnumerationChange.GetLearnedForgottenKnowledge
title: ISyncFullEnumerationChange::GetLearnedForgottenKnowledge (winsync.h)
description: Gets the forgotten knowledge that the destination replica learns when the destination provider applies this change during recovery synchronization.
helpviewer_keywords: ["GetLearnedForgottenKnowledge","GetLearnedForgottenKnowledge method [Windows Sync]","GetLearnedForgottenKnowledge method [Windows Sync]","ISyncFullEnumerationChange interface","ISyncFullEnumerationChange interface [Windows Sync]","GetLearnedForgottenKnowledge method","ISyncFullEnumerationChange.GetLearnedForgottenKnowledge","ISyncFullEnumerationChange::GetLearnedForgottenKnowledge","winsync.isyncfullenumerationchange_getlearnedforgottenknowledge","winsync/ISyncFullEnumerationChange::GetLearnedForgottenKnowledge"]
old-location: winsync\isyncfullenumerationchange_getlearnedforgottenknowledge.htm
tech.root: winsync
ms.assetid: 958bca82-67a7-401f-a9d3-a17f60496cba
ms.date: 12/05/2018
ms.keywords: GetLearnedForgottenKnowledge, GetLearnedForgottenKnowledge method [Windows Sync], GetLearnedForgottenKnowledge method [Windows Sync],ISyncFullEnumerationChange interface, ISyncFullEnumerationChange interface [Windows Sync],GetLearnedForgottenKnowledge method, ISyncFullEnumerationChange.GetLearnedForgottenKnowledge, ISyncFullEnumerationChange::GetLearnedForgottenKnowledge, winsync.isyncfullenumerationchange_getlearnedforgottenknowledge, winsync/ISyncFullEnumerationChange::GetLearnedForgottenKnowledge
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
 - ISyncFullEnumerationChange::GetLearnedForgottenKnowledge
 - winsync/ISyncFullEnumerationChange::GetLearnedForgottenKnowledge
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
 - ISyncFullEnumerationChange.GetLearnedForgottenKnowledge
---

# ISyncFullEnumerationChange::GetLearnedForgottenKnowledge


## -description

Gets the forgotten knowledge that the destination replica learns when the destination provider applies this change during recovery synchronization.

## -parameters

### -param ppLearnedForgottenKnowledge [out]

The forgotten knowledge that the destination replica learns when the destination provider applies this change during recovery synchronization.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This object does not contain source forgotten knowledge. In this case, <i>ppLearnedForgottenKnowledge</i> will return <b>NULL</b>.

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
</table>

## -remarks

The knowledge returned in <i>ppLearnedForgottenKnowledge</i> is the source forgotten knowledge of the change batch projected onto the item that is associated with this change.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchange">ISyncFullEnumerationChange Interface</a>